---
title: Documentation
area: docs
layout: default
section: docs
---

## Tutorials

<div class="tutorials">
    {% for tutorial in site.data.tutorials %}
        <div class="tutorial">
            <a href="{{ tutorial.url }}">
                <img src="{{ tutorial.image }}" alt="{{ tutorial.title }}">
                <h4>{{ tutorial.title }}</h4>
            </a>
            <p class="description">{{ tutorial.description }}</p>
        </div>
    {% endfor %}
</div>

We are actively working on additional tutorials. Thanks for your patience.

## Documentation

### Disney BRDF and Material

Disney's principled BRDF model is available in appleseed in two forms: as a standard appleseed BRDF, and as a custom layered material.

The best reference for the Disney reflection model is probably
[RenderMan's PxrDisney documentation](http://renderman.pixar.com/resources/current/RenderMan/PxrDisney.html).

### SeExpr

appleseed's Disney material allows using arbitrary expressions for any of its inputs. Expressions follow Disney's SeExpr syntax.
Please refer the [SeExpr User Documentation](http://wdas.github.io/SeExpr/doxygen/userdoc.html) for details.

### appleseed Tools

- [makefluffy](/docs/makefluffy.html)

## Conference Materials

### FMX 2015

Franz was invited by [Filmakademie](http://www.filmakademie.de/en/main-page/) to present appleseed at [FMX](http://fmx.de/) 2015 during a one hour talk.

Here are the slides and the appleseed.studio lookdev video used during the talk:

* Slides (PowerPoint 2013): [appleseed-fmx-2015-no-videos.pptx](/docs/fmx/2015/appleseed-fmx-2015-no-videos.pptx)
* Slides with comments (PDF): [appleseed-fmx-2015-slides-comments.pdf](/docs/fmx/2015/appleseed-fmx-2015-slides-comments.pdf)
* Higher quality slides without comments (PDF): [appleseed-fmx-2015-slides-no-comments.pdf](/docs/fmx/2015/appleseed-fmx-2015-slides-no-comments.pdf)
* Lookdev screencast shown during the talk: [Interactive lookdev inside appleseed.studio](https://vimeo.com/127622613)


<!---

## Tutorials

- [Render Layers Assignment Rules](/docs/tutorials/renderlayers.html)

## Tools

### appleseed.studio

### appleseed.cli

### appleseed Tools

- animatecamera
- convertmeshfile
- dumpmetadata
- [makefluffy](/docs/makefluffy.html)
- maketiledexr
- rendermany.py
- updatemany.py
- updateprojectfile

### OSL Tools

- maketx
- oslc
- oslinfo

### Dropbox-Based Render Farm

- rendermanager.py
- rendernode.py

## Open Shading Language

- [OSL Support Status](/docs/oslsupportstatus.html)

-->
