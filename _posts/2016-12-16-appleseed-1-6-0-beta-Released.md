---
title: appleseed 1.6.0-beta Released
---

**TL;DR: We just released [appleseed 1.6.0-beta](https://github.com/appleseedhq/appleseed/releases/tag/1.6.0-beta) and [appleseed-max 0.2.0](https://github.com/appleseedhq/appleseed-max/releases/tag/0.2.0-beta), Gafferseed got a big update in [Gaffer 0.29.0.0](https://github.com/GafferHQ/gaffer/releases/tag/0.29.0.0), and we are developing a new [Maya plugin](https://github.com/appleseedhq/appleseed-maya).**

**We are pleased to announce the release of appleseed 1.6.0-beta**, the sixth release of our beta program and the 29th release overall. Please check out the [release notes](https://github.com/appleseedhq/appleseed/releases/tag/1.6.0-beta) for download links and the full list of changes.

This release brings **massive improvements to our subsurface scattering (SSS) implementation**.

SSS in previous releases of appleseed exhibited all kinds of color shifts and, despite being state of the art, was generally difficult to control. **With this release, SSS is robust, predictable and produces great images**.

This release also brings many bug fixes, performance optimizations and smaller additions such as a first set of OSL shaders matching Maya shading nodes as well as support for multiple cameras in projects.

However, **most of the work for this release has happened under the hood**. Here is a partial summary of the code and infrastructure improvements that were achieved in the past few months:

* We switched the entire shading pipeline of appleseed from double-precision to single-precision floating point. It was simply wasteful to do all the shading calculations in double precision. While this switch has no immediate benefit, it paves the way for a faster shading pipeline. The geometric pipeline still uses double precision as this provides a clear robustness advantage.

* We improved our [Travis CI-based continuous build system](https://travis-ci.org/appleseedhq/appleseed) (which builds every single pull request merged into master) by expanding the *build matrix* to both gcc 4.8 and gcc 5.0, both in C++03 and C++11 mode, in preparation to finally switching to C++11 in the next release.

* We improved our [CMake](https://cmake.org/)-based build system to automatically compile all our OSL shaders when building appleseed.

* We improved the [reports](/stuff/2016-12-16/appleseed Test Suite Report.html) from our automatic test suite to allow updating reference images easily. We also added test scenes to check that appleseed with OSL matches appleseed with its built-in shading pipeline.

**We are also releasing appleseed-max 0.2.0**, our high quality native plugin for [Autodesk 3ds Max](http://www.autodesk.com/products/3ds-max/overview) 2015, 2016 and 2017 ([downloads and release notes](https://github.com/appleseedhq/appleseed-max/releases/tag/0.2.0-beta)).

This release adds a few small features, fixes a few bugs and restores compatibility with Windows 7.

Gafferseed, our native integration of appleseed into [Image Engine](http://image-engine.com/)'s lookdev application [Gaffer](http://www.gafferhq.org/), **received a major overhaul and gained many new features in the process.** Please check out [Gaffer 0.29.0.0 release notes](https://github.com/GafferHQ/gaffer/releases/tag/0.29.0.0) for details (note that, as of today, the current version of Gaffer is [0.30.2.0](https://github.com/GafferHQ/gaffer/releases/tag/0.30.2.0)).

Finally, **we have undertaken a complete rewrite of our native Maya plugin** to reach the same level of functionality, stability and code quality expected from projects under the appleseedhq umbrella. The plugin is still at an early stage of development but is moving fast and already producing images. You can track our progress [on the forum](https://forum.appleseedhq.net/t/maya-plugin-development/129/5) or even by [checking the commits on GitHub](https://github.com/appleseedhq/appleseed-maya/commits/master).

Please head over to our [Discourse forum](https://forum.appleseedhq.net/) for your feedback, questions and comments regarding appleseed, appleseed-max, Gafferseed or any other application of the appleseed suite.

**Make sure to [follow us on Twitter](https://twitter.com/appleseedhq) if you want to stay up-to-date with appleseed development!**
