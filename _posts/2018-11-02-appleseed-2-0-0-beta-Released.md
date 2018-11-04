---
title: appleseed 2.0.0-beta Released
---

![Geometry, textures and environment map by [3D Scan Store](https://www.3dscanstore.com/index.php?route=information/information&information_id=16)<br>Scene reconstruction and skin shader by Juan Carlos Gutiérrez.](https://user-images.githubusercontent.com/321290/47671428-c7a46680-dbaf-11e8-97b2-79afeb54992d.png)

**We are proud to announce the release of appleseed 2.0.0-beta**, the eleventh release of our beta program and the 34th public release since the first alpha in July 2010.

This release is the fruit of relentless design, development, testing and coordination efforts by the appleseed team, an international group of volunteers dedicated to building state-of-the-art open source rendering technology.

**Make sure to read the [core engine release notes](https://github.com/appleseedhq/appleseed/releases/tag/2.0.0-beta) for the full illustrated story!**

Downloads and release notes:

- **[appleseed 2.0.0-beta](https://github.com/appleseedhq/appleseed/releases/tag/2.0.0-beta)**
- **[appleseed for Maya 1.2.0-beta](https://github.com/appleseedhq/appleseed-maya/releases/tag/1.2.0-beta)**
- **[appleseed for 3ds Max 1.0.0-beta](https://github.com/appleseedhq/appleseed-max/releases/tag/1.0.0-beta)**
- **[appleseed for Blender 1.0.0-beta](https://github.com/appleseedhq/blenderseed/releases/tag/1.0.0-beta)**

**We have redoubled our efforts over the past year to provide high-quality native integrations of appleseed into leading DCC apps.** This release continues the trend and integrations now expose the majority of the features available in the core engine.

Among a multitude of other additions and improvements:
- Thanks to a major re-architecture around appleseed's Python bindings, the Blender plugin now offers interactive rendering, AOV support and increased stability and performance.
- The Autodesk® 3ds Max® plugin now features volumetric rendering, denoising, shading overrides, configurable pixel filtering and per ray-type bounce limits.
- The Autodesk® Maya® plugin now features AOV support, support for color and curve ramps, render stamp support and a redesigned Render Settings user interface.

**The core engine has also received a lot of attention**, with significant work from our three Google Summer of Code 2018 students:
- **Kevin Masson implemented a new state-of-the-art adaptive tile sampler** that provides much better performance than the former adaptive pixel sampler (which is deprecated in this release). Kevin Masson has contributed several other exciting features before, during and after the program; they will be available in the next release.
- **Fedor Matantsev implemented a new ray tracing backend based on [Embree](https://embree.github.io/)**, a highly optimized ray tracing library by Intel®. This new backend is still experimental. It should be faster and more robust in the next release of appleseed.
- **Girish Ramesh continued the work started by his predecessor, Srinath Ravichandran, on hair and curve rendering**, with many improvements to curve representation, storage and intersection. While some of these improvements are included in this release, the work to provide a complete workflow around curve rendering is still ongoing.

This release brings many other changes to the core engine:
- **We greatly improved our random-walk subsurface scattering implementation**. The render at the beginning of this post is a fine illustration of the results that can be achieved using appleseed's random-walk SSS.
- **We took our first steps into the world of non-photorealistic rendering (NPR)** with an OSL shader implementing cartoon shading and another one implementing contour rendering.
- **We continued our work on visualization tools**, with rectangular selection of light paths, false colors, relative luminance isolines, etc.

This is a mere glance at what's new in this release. The illustrated core engine release notes and the plugins' release notes contain a lot more details.

**Please give appleseed and the plugins a try** and let us know what works, what doesn't and how we can make appleseed better and more useful to _you_. Feel free to reach out on our [forum](https://forum.appleseedhq.net/), on [Discord](https://discordapp.com/invite/Vcu5A7h) or on [Twitter](https://twitter.com/appleseedhq).