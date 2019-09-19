---
title: appleseed 1.8.1-beta Released
layout: post
section: news illustrated
---

![[Interior Scene](https://forum.appleseedhq.net/t/interior-scene-from-scratch/362) by Juan Carlos Gutiérrez](/img/renders/jc-interior.png)

**We just released appleseed 1.8.1-beta**, the ninth release of our beta program and the 32nd release since the first alpha in July 2010.

Downloads and release notes:

- [appleseed 1.8.1-beta](https://github.com/appleseedhq/appleseed/releases/tag/1.8.1-beta)  
- [appleseed-maya 1.0.1-beta](https://github.com/appleseedhq/appleseed-maya/releases/tag/1.0.1-beta)  
- [appleseed-max 0.4.7-beta](https://github.com/appleseedhq/appleseed-max/releases/tag/0.4.7-beta)  
- [blenderseed 0.7.0](https://github.com/appleseedhq/blenderseed/releases/tag/v0.7.0)  

**This release introduces a _massively_ improved Blender plugin** thanks to the downright obsessive work of Jon Dent and Luke Kliber:

- Entirely redesigned the plugin's user interface
- Removed the need to set a project folder
- Added all missing BSDF models
- Made render buckets visible
- Made the render progress bar functional
- Exposed the orthographic camera
- Removed obsolete features
- Fixed _Many. Dozens. Bugs._

**Our Autodesk® 3ds Max® plugin also got its share of attention** thanks to the mad work of Sergo Pogosyan and the valuable inputs of our beta testers:

- Added physically-based plastic and metal materials
- Introduced a blend material to blend up to 10 materials together
- Added a log window displaying appleseed's debug and warning messages during rendering
- Fixed many bugs

**Our Autodesk® Maya® plugin was noticeably improved as well** thanks to coding machines Esteban Tovagliari and Luis Barrancos:

- Added support for SSS sets, allowing to group translucent objects using arbitrarily named tags
- Implemented swatch rendering in the Hypershade window
- Improved interactivity when rendering to the RenderView
- Fixed several bugs

Finally, the core renderer and associated tools received a number of important bug fixes and improvements as well as the introduction of **energy compensation** in the glossy and metal BRDFs.

As usual, **please give appleseed and the plugins a try** and let us know what works, what doesn't and how we can make appleseed better and more useful to _you_. Feel free to reach out on our [users forum](https://forum.appleseedhq.net/) or via [Twitter](https://twitter.com/appleseedhq).
