---
title: Documentation - Render Layers Assignment Rules
area: docs
layout: docs
---

## Render Layers Assignment Rules

Regular expression render layer rules match on [entity paths](Terminology#entity-path).

The `entity_type` parameter allows to restrict matching to a certain type of entities. The following entity types are supported: `assembly`, `assembly_instance`, `edf`, `environment_edf`, `environment_shader`, `light`, `material`, `object`, `object_instance`, `surface_shader`.

Regular expression patterns use the Perl syntax: [cheat sheet](http://www.cs.tut.fi/~jkorpela/perl/regexp.html), [examples](http://www.cs.tut.fi/~jkorpela/perl/regexp.html#ex).

An important note: at the moment, AOVs only get rendered in Final Rendering mode, not in Interactive Rendering mode.

Let's use the built-in Cornell Box for an example: open the scene (File &rarr; Open Built-in Project &rarr; Cornell Box), then create a new Render Layer Assignment rule (right-click on Project &rarr; Rules &rarr; Render Layer Assignments in the Project Explorer). Enter `short block` in the `Render Layer` field. Enter `short_block` for the `Pattern` field. Leave `Entity Type` to `All`.

![Regular Expression Render Layer Assignment Rule Dialog](https://raw.githubusercontent.com/appleseedhq/appleseed-wiki/master/images/render-layers-tutorial/regexp-render-layer-dialog.png)

This rule will match the `short_block` object and place it into its own render layer. Render in Final Rendering mode (F6 in appleseed.studio). Click on the *Save All AOVs...* toolbar button above the rendered image and enter a filename (e.g. `cb.exr`). Two files will get created: `cb.exr` and `cb.short_block.exr`:

![Cornell Box AOVs](https://raw.githubusercontent.com/appleseedhq/appleseed-wiki/master/images/render-layers-tutorial/cornell-box-aovs.png)

Note that while the main output (`cb.exr`) uses the color space defined in the frame (sRGB in the case of the built-in Cornell Box), all AOVs are always expressed in linear RGB.
