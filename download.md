---
title: Download
area: download
layout: default
section: download
---

## appleseed

{% for release in site.data.releases limit:1 %}

The current version of appleseed is {{ release.version }}. It was released on {{ release.date }}.

Please check the [release notes]({{ release.github }}) for the list of new features and bug fixes available in this version.

<div class="builds">
    {% for build in release.builds %}
        <a class="build" href="{{ build.url }}" download>
            {% case build.platform %}
                {% when 'windows' %}
                    <i class="fa fa-windows"></i>
                {% when 'linux' %}
                    <i class="fa fa-linux"></i>
                {% when 'osx' %}
                    <i class="fa fa-apple"></i>
            {% endcase %}
            <div>{{ build.label }}</div>
        </a>
    {% endfor %}
</div>

Intermediate, preview releases are also regularly made available from the [Releases](https://github.com/appleseedhq/appleseed/releases) page on GitHub.

Follow us on [Twitter](https://twitter.com/appleseedhq) to get notified of new releases.

{% endfor %}

## Demo Scenes

<div class="scenes">
    {% for scene in site.data.scenes %}
        <a class="scene" href="{{ scene.url }}">
            <img src="{{ scene.image }}" alt="{{ scene.name }}">
            <div>{{ scene.name }}</div>
        </a>
    {% endfor %}
</div>

## Source Code

Visit the [GitHub page](https://github.com/appleseedhq/appleseed) to&hellip;

- clone or fork the appleseed repository
- browse the source code online
- download the source code for a particular revision as a zip file

Note that the preferred way to obtain appleseed source code is to clone the Git repository hosted on GitHub.
This will allow you to stay in sync with the latest updates and fixes as soon as we pushed them to GitHub.

If you're planning on building appleseed yourself, make sure to check out our detailed
[compilation guide](https://github.com/appleseedhq/appleseed/wiki/Building-appleseed).

## Exporters & Integrations

### appleseed-max

appleseed-max is a native plugin for Autodesk 3ds Max 2015/2016.

- [Releases](https://github.com/appleseedhq/appleseed-max/releases)
- [Progress updates and development builds](https://forum.appleseedhq.net/t/3ds-max-plugin-development/109)
- [GitHub repository](https://github.com/appleseedhq/appleseed-max)

### appleseed-maya

appleseed-maya is a native plugin for Autodesk Maya 2015/2016 currently in development.

- [Features and documentation](http://appleseed-maya.readthedocs.org/en/latest/)
- [GitHub repository](https://github.com/appleseedhq/appleseed-maya)

### blenderseed

blenderseed is a appleseed plugin for Blender.

- [Download the latest version](https://github.com/appleseedhq/blenderseed/releases/latest)
- [Installation instructions and documentation](https://github.com/appleseedhq/blenderseed/wiki)
- [GitHub repository](https://github.com/appleseedhq/blenderseed)
