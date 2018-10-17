---
title: Documentation - appleseed.studio
area: docs
layout: docs
---

## appleseed.studio


### Introduction

appleseed.studio is a graphical application to inspect, debug, tweak and render scenes.


### Keyboard Shortcuts

LMB = left mouse button  
MMB = middle mouse button  
RMB = right mouse button

**Warning:** on macOS, replace <kbd>Ctrl</kbd> by <kbd>Cmd</kbd>.


#### Files

Keys | Action
---- | ------
<kbd>Ctrl+N</kbd> | New project
<kbd>Ctrl+O</kbd> | Open project
<kbd>Ctrl+R</kbd> | Reload project
<kbd>Ctrl+S</kbd> | Save project

#### Main Interface

Keys | Action
---- | ------
<kbd>F11</kbd> | Show/hide all panels
<kbd>Ctrl+Shift+S</kbd> | Save appleseed.studio settings
<kbd>Ctrl+Shift+R</kbd> | Reload appleseed.studio settings
<kbd>Escape</kbd> | Cancel and close window

#### Entity Editor

<kbd>Enter</kbd> | Apply changes
<kbd>Ctrl+Enter</kbd> | Apply changes and close window

#### Viewport

Keys | Action
---- | ------
<kbd>Ctrl+LMB+drag</kbd> | Rotate camera
<kbd>Ctrl+MMB+drag</kbd> | Truck camera
<kbd>Ctrl+RMB+drag</kbd> | Dolly camera
<kbd>Shift+LMB+drag</kbd> | Move render in viewport
<kbd>Shift+LMB</kbd> | Focus on viewport
<kbd>LMB</kbd> | Select entity (based on entity picking mode)
<kbd>Del</kbd> | Delete selected entity

  
The following shortcuts require that you first focus on the viewport by pressing <kbd>Shift</kbd> and clicking with the left mouse button on the render:

Keys | Action
---- | ------
<kbd>Ctrl+C</kbd> | Copy render to clipboard
<kbd>F</kbd> | Frame selected object
<kbd>R</kbd> | Set render region
<kbd>C</kbd> | Clear render region
<kbd>X</kbd> | Clear frame
<kbd>I</kbd> | Toggle pixel inspector
<kbd>+</kbd> | Zoom in
<kbd>-</kbd> | Zoom out
<kbd>*</kbd> | Reset zoom

#### Rendering

Keys | Action
---- | ------
<kbd>F5</kbd> | Start interactive rendering
<kbd>F6</kbd> | Start final rendering
<kbd>Shift+F5</kbd> | Stop interactive/final rendering
<kbd>F7</kbd> | Rendering settings
<kbd>Ctrl+Shift+1</kbd> | Color diagnostic mode
<kbd>Ctrl+Shift+2</kbd> | Coverage diagnostic mode
<kbd>Ctrl+Shift+3</kbd> | Barycentric coordinates diagnostic mode
<kbd>Ctrl+Shift+4</kbd> | UV coordinates diagnostic mode
<kbd>Ctrl+Shift+5</kbd> | Tangents diagnostic mode
<kbd>Ctrl+Shift+6</kbd> | Bitangents diagnostic mode
<kbd>Ctrl+Shift+7</kbd> | Geometric normals diagnostic mode
<kbd>Ctrl+Shift+8</kbd> | Shading normals diagnostic mode
<kbd>Ctrl+Shift+9</kbd> | Unmodified shading normals [1] diagnostic mode

[1] Unmodified shading normals are shading normals before bump/normal mapping has been applied.

#### Debugging

Keys | Action
---- | ------
<kbd>Ctrl+Shift+T</kbd> | Open unit tests window
<kbd>Ctrl+Shift+B</kbd> | Open unit benchmarks window
