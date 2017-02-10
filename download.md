---
title: Download
area: download
layout: default
section: download
---

## appleseed

{% for release in site.data.releases limit:1 %}

The latest version is **appleseed {{ release.version }}**. It was released on {{ release.date }}.

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

## Integrations

&nbsp;
{: .gaffer-logo}

appleseed is the default renderer of [Gaffer](http://www.gafferhq.org/) by [Image Engine](http://image-engine.com/).

Gaffer is a general purpose node-based application designed for use in the visual effects industry.

It provides basic tools for procedural scene generation, shader authoring, rendering, and image compositing.

### Autodesk® 3ds Max®
{: .max-logo}

**appleseed-max** is a native plugin for [Autodesk® 3ds Max®](http://www.autodesk.com/products/3ds-max/overview) 2015, 2016 and 2017.

- [**Downloads**](https://github.com/appleseedhq/appleseed-max/releases)
- [GitHub repository](https://github.com/appleseedhq/appleseed-max)
- [Progress updates and development builds](https://forum.appleseedhq.net/t/3ds-max-plugin-development/109)

### Autodesk® Maya®
{: .maya-logo}

**appleseed-maya** is a native plugin for [Autodesk® Maya®](http://www.autodesk.com/products/maya/overview) 2015, 2016 and 2017 currently in development.

- [GitHub repository](https://github.com/appleseedhq/appleseed-maya)
- [Progress updates](https://forum.appleseedhq.net/t/maya-plugin-development/129)

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

![GitHub Octocat Logo](/img/github-octocat-logo.png)

Visit the [GitHub page](https://github.com/appleseedhq/appleseed) to&hellip;

- clone or fork the appleseed repository
- browse the source code online
- download the source code for a particular revision as a zip file

Note that the preferred way to obtain appleseed source code is to clone the Git repository hosted on GitHub.
This will allow you to stay in sync with the latest updates and fixes as soon as we pushed them to GitHub.

Make sure to follow our detailed [build instructions](https://github.com/appleseedhq/appleseed/wiki/Building-appleseed) if you want to build appleseed from sources.
