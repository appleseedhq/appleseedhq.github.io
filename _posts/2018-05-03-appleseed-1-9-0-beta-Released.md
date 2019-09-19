---
title: appleseed 1.9.0-beta Released
layout: post
section: news illustrated
---

![Red Paper Boat by [Giuseppe Lucido](https://zaldor.artstation.com/)](https://user-images.githubusercontent.com/321290/39409337-af8fa122-4be5-11e8-8697-1c8188681502.jpg)

**We are proud to announce the release of appleseed 1.9.0-beta**, the tenth release of our beta program and the 33rd public release since the first alpha in July 2010.

**Make sure to read the [main release notes](https://github.com/appleseedhq/appleseed/releases/tag/1.9.0-beta) for the full illustrated story!**

Downloads and release notes:

- [appleseed 1.9.0-beta](https://github.com/appleseedhq/appleseed/releases/tag/1.9.0-beta)  
- [appleseed-maya 1.1.0-beta](https://github.com/appleseedhq/appleseed-maya/releases/tag/1.1.0-beta)  
- [appleseed-max 0.5.0-beta](https://github.com/appleseedhq/appleseed-max/releases/tag/0.5.0-beta)  
- [blenderseed 0.8.0-beta](https://github.com/appleseedhq/blenderseed/releases/tag/0.8.0-beta)  

This release is the result of relentless design, development, testing and coordination efforts by the appleseed team, an international group of volunteers dedicated to building state-of-the-art open source rendering technology.

A renderer is of no use without easy-to-use integrations into digital content creation applications, so for the past couple years we've been dedicating a sizable chunk of our resources to develop an ecosystem of high-quality plugins for 3ds Max, Maya, Blender and Gaffer. **This release continues the trend and introduces _major_ improvements to the 3ds Max and Blender plugins**. Please check out the release notes of the individual plugins for details.

**One major new feature of the 3ds Max and Blender plugins is full native support for appleseed's high-quality OSL shaders.** This means that, starting with this release, all plugins now expose the same set of OSL materials, creating exciting new opportunities for future releases such as seamless exchange of materials and even complete scenes between plugins.

**A major new feature introduced in this release is the integration of BCD, a powerful new denoiser** specifically designed to remove noise from final frame renders.

**Another important feature of this release is a new light paths capture, visualization and export system** that allows to explore interactively and in great details how light scatters in a scene. This feature is part of a greater industrial project between the appleseed team and a major international group. We've made a short video to illustrate this feature, make sure to check it out: [Light Path Capture on the Hubble Space Satellite](https://vimeo.com/263532331).

**We've also kickstarted an effort to lower the barrier to entry to use appleseed** by removing superfluous parameters, by adopting better defaults and by renaming parameters and settings to make their effect more intuitive. We're at the beginning of this effort and there's a lot more to do, but that's the direction we're following.

As usual, **please give appleseed and the plugins a try** and let us know what works, what doesn't and how we can make appleseed better and more useful to _you_. Feel free to reach out on our [forum](https://forum.appleseedhq.net/), on [Discord](https://discordapp.com/invite/Vcu5A7h) or via [Twitter](https://twitter.com/appleseedhq).