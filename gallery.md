---
title: Gallery
area: gallery
layout: default
section: gallery
---

## Renders

<div class="image-gallery">
    {% for item in site.data.renders %}
        <a href="{{ item.url }}">
            <img src="{{ item.url }}" alt="{{ item.legend | markdownify | strip_html }}">
        </a>
    {% endfor %}
</div>

## Screenshots

<div class="image-gallery">
    {% for item in site.data.screenshots %}
        <a href="{{ item.url }}">
            <img src="{{ item.url }}" alt="{{ item.legend | markdownify | strip_html }}">
        </a>
    {% endfor %}
</div>

<script type="text/javascript">
    $(window).load(function () {
        $(".image-gallery").packery({
            itemSelector: "a",
            gutter: 10
        });
    });

    $(".image-gallery").photobox("a");
</script>
