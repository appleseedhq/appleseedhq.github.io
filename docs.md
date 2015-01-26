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
                <p class="description">{{ tutorial.description }}</p>
            </a>
        </div>
    {% endfor %}
</div>

We are actively working on additional tutorials. Thanks for your patience.

## Documentation

### appleseed Tools

- [makefluffy](/docs/makefluffy.html)

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
