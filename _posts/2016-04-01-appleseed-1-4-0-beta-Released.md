---
title: appleseed 1.4.0-beta Released
layout: post
section: news illustrated
---

We are pleased to announce the release of appleseed 1.4.0-beta, the fourth release of our beta program and the 27th release overall. Check out the [release notes](https://github.com/appleseedhq/appleseed/releases/tag/1.4.0-beta) for the full list of changes.

The big focus of this release was improving our support for transparent materials: we implemented full support for nested dielectrics which, together with automatic tracking of indices of refractions, considerably simplifies the construction of scenes with complex nested transparent volumes.

For good measure, we also added a new advanced glass BSDF and a state-of-the-art metal BRDF based on recent research (both also available as OSL closures). You can see examples of these new BRDFs in the release notes.

Of course, this release includes numerous other changes and improvements, like a much improved OSL shader library, refinements of appleseed.studio's user interface, and the usual assortment of bug fixes and performance improvements.

As usual, this new release of appleseed is simultaneously available on Windows, OS X and Linux.

Please head over to our [Discourse forum](https://forum.appleseedhq.net/) for your feedback, questions and comments.

And make sure to [follow us on Twitter](https://twitter.com/appleseedhq) if you want to stay up-to-date with appleseed development!
