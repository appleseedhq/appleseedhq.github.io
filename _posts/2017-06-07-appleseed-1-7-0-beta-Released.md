---
title: appleseed 1.7.0-beta Released
---

![New physically-based plastic BRDF<br>(Coffee Maker by Blend Swap user [cekuhnen](http://www.blendswap.com/user/cekuhnen))](/img/renders/coffeemaker.jpg)

**We are pleased to announce the release of [appleseed 1.7.0-beta](https://github.com/appleseedhq/appleseed/releases/tag/1.7.0-beta)**, the seventh release of our beta program and the 30th release overall. Please check out the [release notes](https://github.com/appleseedhq/appleseed/releases/tag/1.7.0-beta) for download links and the full list of changes.

**This release is the result of the hard and relentless work of an amazing team.** I (Franz) am deeply proud as well as grateful for the consistent high quality work produced every day. It is truly an honor to work with you guys!

We would like to use this opportunity to congratulate and thank our Google Summer of Code 2017 students *Artem Bishev*, *Petra Gospodnetic* and *Gleb Mishchenko* who all three contributed significant features before even being accepted into the program. We are also grateful to the GSoC candidates that we unfortunately could not mentor this year but who nevertheless contributed to this release: *Aytek Aman*, *Andreea Dincu*, *Andrei Ivashchenko*, *Nabil Miri*, *Kutay Macit*, *Aakash Praliya* and *Animesh Tewari*.

**With this release, we made considerable efforts to further refine our ray traced subsurface scattering implementation.** The results are now more accurate and consistent. We also took this opportunity to add support for SSS sets that allow merging or separating translucent objects. Furthermore, we modified the Gaussian BSSRDF to expose the same parameters as other BSSRDF models; this makes finding the right BSSRDF model much easier. Finally, we added Fresnel weight parameters to all BSSRDF models and we exposed the Gaussian BSSRDF to OSL.

**We have significantly enriched our OSL shader library.** In particular, we are nearing completion on a massive effort to reimplement Maya shading nodes as OSL shaders. We will give a lot more details about this work when we announce the first release (soon!) of [appleseed-maya](https://github.com/appleseedhq/appleseed-maya), our new native plugin for Autodesk® Maya®.

**The path tracer now offers additional performance controls:** we added distinct diffuse/glossy/specular bounce limits in addition to the existing global limit, and we introduced a *Low Light Threshold* parameter that allows to skip low-contributing light samples (and thus to eliminate costly shadow rays) without introducing bias.

This release brings many other features such as a new physically-based plastic BRDF, a completely redesigned AOV mechanism, initial support for archive assemblies, support for many more texture formats thanks to the full switch to [OpenImageIO](https://github.com/OpenImageIO/oiio) for texture loading, and many more improvements, refinements, fixes and cleanups to appleseed core, appleseed.studio and appleseed.python.

**Finally, we are also pleased to announce the release of [appleseed-max 0.4.5](https://github.com/appleseedhq/appleseed-max/releases/tag/0.4.5-beta)**, our native plugin for Autodesk® 3ds Max® 2015/2016/2017. This release brings a host of new features such as environment map support, appleseed object properties (as an Object Modifier), support for render regions, and several bug fixes and improvements. Many thanks to *Sergo Pogosyan* for the hard work on the plugin!
