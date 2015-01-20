---
layout: default
title: Download
section: download
---

## appleseed

{% for release in site.data.releases limit:1 %}

The current version of appleseed is {{ release.version }}. It was released on {{ release.date }}.

Please check the [release notes]({{ release.github }}) for the list of new features and bug fixes available in this version.

Download appleseed {{ release.version }} for your platform:

<div class="builds">
{% for build in release.builds %}
    <div class="build">
    {% case build.platform %}
        {% when 'windows' %}
            <a href="{{ build.url }}" download><i class="fa fa-windows"></i></a>
            <div>Windows Vista and Later</div>
        {% when 'linux' %}
            <a href="{{ build.url }}" download><i class="fa fa-linux"></i></a>
            <div>Linux</div>
        {% when 'osx' %}
            <a href="{{ build.url }}" download><i class="fa fa-apple"></i></a>
            <div>OS X 10.9 and Later</div>
        {% endcase %}
    </div>
{% endfor %}
</div>

{% endfor %}

## Demo Scenes

Coming soon!

## Source Code

Visit the [<i class="fa fa-github"></i> GitHub page](https://github.com/appleseedhq/appleseed) to&hellip;

- clone or fork the appleseed repository
- browse the source code online
- download the source code for a particular revision as a zip file

Note that the preferred way to obtain appleseed source code is to clone the Git repository hosted on GitHub.
This will allow you to stay in sync with the latest updates and fixes as soon as we pushed them to GitHub.

If you're planning on building appleseed yourself, make sure to check out our detailed
[compilation guide](https://github.com/appleseedhq/appleseed/wiki/Building-appleseed).
