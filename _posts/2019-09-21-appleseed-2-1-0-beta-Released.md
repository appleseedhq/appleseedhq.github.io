---
title: appleseed 2.1.0-beta Released
layout: post
section: news illustrated
---

![Ajax bust by Torolf Sauermann (jotero), render by Juan Carlos Gutiérrez](/img/posts/ajax-bust.png)

**We are proud to announce the release of appleseed 2.1.0-beta**, the twelveth release of our beta program and the 35th public release since the first alpha in July 2010.

This release is the fruit of relentless design, development, testing and coordination efforts by [the appleseed team](/about.html#team), an international group of volunteers dedicated to building state-of-the-art open source rendering technology.

**Make sure to read the [core engine release notes](https://github.com/appleseedhq/appleseed/releases/tag/2.1.0-beta) for the full illustrated story!**

Downloads and release notes:

- **[appleseed 2.1.0-beta](https://github.com/appleseedhq/appleseed/releases/tag/2.1.0-beta)**
- **[appleseed for Maya 1.3.0-beta](https://github.com/appleseedhq/appleseed-maya/releases/tag/1.3.0-beta)**
- **[appleseed for 3ds Max 1.1.0-beta](https://github.com/appleseedhq/appleseed-max/releases/tag/1.1.0-beta)**
- **[appleseed for Blender 2.0.0-beta](https://github.com/appleseedhq/blenderseed/releases/tag/2.0.0-beta)**

We sure have been quiet during the past ten months, but as you'll see it wasn't for a lack of activity! The team has been hard at work and everyone is proud of what we accomplished since the last release.

Once again, our focus in this release has been on improving our native plugins for Autodesk® 3ds Max®, Autodesk® Maya® and Blender. Of course, the core engine, appleseed.studio and the suite of command line tools have all received their share of attention with more than a hundred new features and bug fixes. Let's go over some highlights of this release.

The core rendering engine received a number of important new features in this release:

- Sergo Pogosyan added **full support for [Cryptomatte](https://github.com/Psyop/Cryptomatte)** in the form of a new set of AOVs.

- Google Summer of Code (GSoC) 2018 student and GSoC 2019 mentor Kevin Masson implemented **render checkpointing**, a mechanism to resume multi-pass renders after they were interrupted and to add rendering passes to a finished render. Example workflows using this feature are detailed in the release notes.

- Thanks to Esteban Tovagliari, **appleseed is now able to compile [OpenShadingLanguage](https://github.com/imageworks/OpenShadingLanguage) (OSL) shaders on the fly**. This unlocks the possibility for users to write some OSL code in their DCC application of choice and see the results in the render immediately, without to manually compile the OSL shader with the command line compiler. Our Blender plugin exposes this feature; other plugins will implement similar workflows in future releases.

- Esteban also switched appleseed to use **Filter Importance Sampling** instead of filtered sample splatting. This led to several performance improvements, but it also unlocked the ability to use modern denoisers such as [Intel® Open Image Denoise](https://openimagedenoise.github.io/) on appleseed renders.

On the plugins front, Jon Dent led a **major effort to rearchitect our Blender plugin**, with three main achievements:

- The plugin now supports **both Blender 2.79 and Blender 2.80+** (with separate packages). We also tested the plugin with Blender 2.81 and it appears to work fine.

- **Exports are up to an order of magnitude** faster thanks to a complete rewrite of the core geometry export code in C++.

- Texture conversion to the high performance `*.tx` format is now **faster, friendlier and more robust** as it no longer relies on invoking the `maketx` command line utility; instead, texture conversion is now implemented on the C++ side of the plugin.

Jon also exposed Cryptomatte AOVs, stereoscopic and fisheye lens cameras and added an OSL scripting node that relies on appleseed's newfound ability to compile OSL shaders on the fly.

**Our Autodesk® 3ds Max® plugin** has also been vastly improved by Herbert Crepaz and Sergo Pogosyan, with more than two dozen new features and bug fixes, among which support for 3ds Max 2020, object and camera transformation motion blur, Cryptomatte AOVs and Stochastic Progressive Photon Mapping (SPPM) support.

Finally, in-house mad scientist Herbert Crepaz also added many new features to our **Autodesk® Maya® plugin** such as Maya 2019 support, Cryptomatte AOVs and SPPM.

The team added many other features and fixed many bugs in all pieces of the appleseed ecosystem, and this post merely scratches the surface. Please check the various release notes for the full picture!

**Looking forward**, we have several exciting new features coming up in the next release of appleseed thanks to the amazing work of our Google Summer of Code 2019 students Stephen Agyemang and Gray Olson:

- Stephen worked on implementing **Practical Path Guiding**, a novel technique that extends our unidirectional path tracer and lets it learn the distribution of incoming light in order to trace paths toward more relevant areas of the scene and improve its performance with indirect lighting. You can find a lot more details about this technique in [Stephen's final report](https://github.com/BashPrince/GSoC-2019-Final-Report).

- Gray improved our innovative **light path recording and visualization** technology. Thanks to Gray's work, the next version of appleseed will allow to overlay light paths over the final render. It will also display light paths using a modern OpenGL profile, with proper antialiasing and transparency. Finally, it will let users filter light paths using [Light Path Expressions](https://github.com/imageworks/OpenShadingLanguage/wiki/OSL-Light-Path-Expressions), an industry standard for expressing paths of interest. Check out [Gray's final report](https://www.grayolson.me/blog/posts/gsoc-2019/) for details and pictures.

Also in the pipe are a number of major features and improvements, among which support for heterogenous volumes and for [OpenVDB](https://www.openvdb.org/) files, and a state-of-the-art hair shading model and corresponding OSL shader.

All these features and improvements are already implemented and working. They will be merged into appleseed over the coming weeks and will be available to end users in the next version of appleseed. Stay tuned!

**If you give appleseed and the plugins a try**, please let us know what works, what doesn't and how we can make appleseed better and more useful to you. Feel free to reach out on our [forum](https://forum.appleseedhq.net/), on [Discord](https://discordapp.com/invite/Vcu5A7h) or on [Twitter](https://twitter.com/appleseedhq).
