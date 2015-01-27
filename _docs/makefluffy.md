---
title: Documentation - makefluffy
area: docs
layout: docs
---

## makefluffy


### Introduction

Starting with version 1.1.0 alpha-22, appleseed ships with a new command line tool called `makefluffy`. The purpose of this tool is to grow hair ("fluff") on any appleseed scene or part of a scene. It is useful to quickly generate a lot of curves in order to test performances and robustness of appleseed's curve rendering.

We call *fluffification* the process of applying `makefluffy` on an object.


### Command Line Arguments

`makefluffy` has a number of required and optional command line arguments. The general syntax is as follow:

    makefluffy [options] input.appleseed output.appleseed

In addition to the usual command line options shared by all appleseed command line tools (`--help`, `--version`, etc.), the following options are available:

    --curves, -n

**Required**. Set the number of curves to generate *per curve object*.

    --length, -l

**Required**. Set the base length of the curves. This value is expressed in object space.

    --root-width, -rw

**Required**. Set the width of the curves at the roots. This value is expressed in object space.

    --tip-width, -tw

**Required**. Set the width of the curves at the tips. This value is expressed in object space. One will usually want the tip width to be smaller than the root width. A good starting point is having `tip width = 1/10 * root width`.

---

    --length-fuzziness, -lf

Optional. Set the amount of fuzziness in the curves length. A value of 0 will result in all curves having exactly the same length. A value of 0.5 means that curves lengths will vary between 50% shorter and 50% longer than the base length. The default value is 0.6. Values greater than 1.0 are allowed.

    --curliness, -c

Optional. Set the amount of curliness of the curves. A value of 0 will result in perfectly straight curves. The default value is 1.5. Values greater than 1.0 are then obviously allowed.

    --presplits, -p

Optional. Set the number of *presplits*, i.e. the number the times curves should be split (in half) when inserted into the object. Splitting curves will result in a larger memory footprint but potentially faster rendering. The default value is 0 (no presplits).

It can be useful to increase this value when generating long, highly overlapping curves. Start with low values (1, 2, etc.) and check memory usage and performance increase. Values above 5 or 6 are suspicious.

    --include, -i

Optional. Grow curves for a subset of the object instances in the scene, as defined by a regular expression following the Perl syntax ([cheat sheet](http://www.cs.tut.fi/~jkorpela/perl/regexp.html), [examples](http://www.cs.tut.fi/~jkorpela/perl/regexp.html#ex)). The default value is `.*` (all object instances are included).

    --exclude, -e

Optional. Exclude object instances who names match a given regular expression from fluffification. The default value is such that no object instance is excluded (technically the default value is `/(?!)/`, which is [designed to never match anything](http://stackoverflow.com/a/4589566/393756)).

You will probably want to exclude a number of object instances from fluffification, such as mesh lights. For instance, if the mesh lights of your input scene are named `light1`, `key light`, `ceiling_light`, etc. you can exclude them all at once by using

    --exclude light

## Example: Fluffy Cornell Box

Let's fluffify the famous [Cornell Box](http://en.wikipedia.org/wiki/Cornell_box):

![Fluffy Cornell Box](/img/docs/fluffycornellbox.jpg)

This image contains 2.8 million curves and was rendered with [spectral rendering](http://en.wikipedia.org/wiki/Spectral_rendering) using measured data from the [official Cornell Box specification](http://www.graphics.cornell.edu/online/box/data.html).

The scene that produced this image was generated using the following command line:

    makefluffy -n 100000 -l 15 -rw 0.001 -tw 0.0001 -p 2 -e light
      fluffy_cornell_box_template.appleseed fluffy_cornell_box.appleseed

where the source scene, `fluffy_cornell_box_template.appleseed`, is a modification of the default Cornell Box where the light has been cut into the ceiling, instead of being placed a few millimeters below it.

We also did the following adjustements on the scene before rendering:

- We increased the light's radiance by a factor of 3 (by setting the Radiance Multiplier parameter to 3 on `light_material_edf`).
- We limited the number of bounces to 3 (by default appleseed with simulate an infinite number of bounces).
- We used a Max Ray Intensity of 0.4 to get rid of the fireflies.


### Conclusion

This is it for this silly tool. Make sure to post your images on the [forum](https://forum.appleseedhq.net/)!
