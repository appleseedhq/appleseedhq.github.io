---
title: Gallery
area: gallery
layout: default
section: gallery
---

## Videos

<div class="collection">
    {% for item in site.data.animations %}
        <a href="{{ item.video }}" rel="video">
            <img src="{{ item.thumbnail }}" alt="{{ item.legend | markdownify | strip_html }}">
        </a>
    {% endfor %}
</div>

## Still Images

<div class="collection">
    {% for item in site.data.stillimages %}
        <a href="{{ item.url }}">
            <img src="{{ item.url | append: '.preview.jpg' }}" alt="{{ item.legend | markdownify | strip_html }}">
        </a>
    {% endfor %}
</div>

## Screenshots

<div class="collection">
    {% for item in site.data.screenshots %}
        <a href="{{ item.url }}">
            <img src="{{ item.url | append: '.preview.jpg' }}" alt="{{ item.legend | markdownify | strip_html }}">
        </a>
    {% endfor %}
</div>

<script>
    "use strict";

    $(window).load(function () {
        $(".collection").packery({
            itemSelector: "a",
            gutter: 10
        });

        $(".collection").photobox("a");
    });
</script>
