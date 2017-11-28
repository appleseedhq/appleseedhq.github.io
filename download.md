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

**appleseed-max** is a native plugin for Autodesk® 3ds Max® 2015, 2016 and 2017.

- [**Downloads**](https://github.com/appleseedhq/appleseed-max/releases)
- [Progress updates and development builds](https://forum.appleseedhq.net/t/3ds-max-plugin-development/109)
- [GitHub repository](https://github.com/appleseedhq/appleseed-max)

### Autodesk® Maya®
{: .maya-logo}

**appleseed-maya** is a native plugin for Autodesk® Maya® 2017 and later.

- [**Downloads**](https://github.com/appleseedhq/appleseed-maya/releases)
- [Documentation](http://appleseed-maya.readthedocs.io/en/latest/)
- [GitHub repository](https://github.com/appleseedhq/appleseed-maya)

## Demo Scenes

<div class="scenes">
    {% for scene in site.data.scenes %}
        <a class="scene" href="{{ scene.url }}">
            <img src="{{ scene.image }}" alt="{{ scene.name }}">
            <div>{{ scene.name }}</div>
        </a>
    {% endfor %}
</div>

## Shaderball

<img src="/img/appleseed-shaderball.png" alt="appleseed shaderball" class="shaderball-render" />

<div class="shaderballs">
    <a class="shaderball" href="https://github.com/appleseedhq/shaderball/releases/download/v4/appleseed_shaderball_v4.zip" download>
        <div class="card">
            <img src="/img/appleseed-seeds-64-gray.png" />
        </div>
        <div>appleseed</div>
    </a>
    <a class="shaderball" href="https://github.com/appleseedhq/shaderball/releases/download/v4/appleseed_shaderball_v4_maya.zip" download>
        <div class="card">
            <img src="/img/autodesk-maya-logo-gray.png" />
        </div>
        <div>Maya® 2015</div>
    </a>
    <a class="shaderball" href="https://github.com/appleseedhq/shaderball/releases/download/v4/appleseed_shaderball_v4_alembic.zip" download>
        <div class="card">
            <img src="/img/alembic-logo.png" />
        </div>
        <div>Alembic cache</div>
    </a>
    <a class="shaderball" href="https://github.com/appleseedhq/shaderball/releases/download/v4/appleseed_shaderball_v4_obj.zip" download>
        <div class="card">
            <img src="/img/obj-logo.png" />
        </div>
        <div>OBJ file</div>
    </a>
</div>

The shaderball, like all our assets, is licensed under the [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.

<div class="license-notice">
    OBJ icon made by <a href="http://www.freepik.com" title="Freepik">Freepik</a> from <a href="http://www.flaticon.com" title="Flaticon">www.flaticon.com</a> licensed under <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a>.
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
