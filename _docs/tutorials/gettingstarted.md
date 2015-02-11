---
title: Documentation - Getting Started
area: docs
layout: docs
---

## Getting Started

Welcome! Thanks for trying out appleseed.

In this guide, you'll learn how to:

- [Download and install appleseed](#downloading-and-installing-appleseed)
- [Start appleseed.studio](#starting-appleseedstudio)
- [Load and render a built-in scene](#loading-and-rendering-a-built-in-scene)
- [Navigate in the scene during interactive rendering](#navigating-in-the-scene)
- [Start a final render](#starting-a-final-render)
- [Change the render settings](#changing-the-render-settings)

And we'll wrap up with some [closing notes](#closing-notes).

Let's get started.


### Downloading and installing appleseed

If you haven't done so already, head to the [Download](/download.html) page and download
the current version of appleseed for your platform.

If a build for your platform does not appear to be available, it might be that we didn't
have a chance to make it yet. In that case, feel free to drop us a line in the
[forum](https://forum.appleseedhq.net/) and we'll try to make a build shortly.

Builds come as plain zip files. Installing appleseed is reduced to simply unzipping the
archive somewhere on your computer. From now on we'll refer to the place you installed
appleseed in as `appleseed`.


### Starting appleseed.studio

appleseed.studio is a graphical environment which allows creating, inspecting, tweaking,
debugging and rendering scenes. Technically, appleseed is only the renderer, it has no
user interface. However, appleseed.studio is the central tool (and the "face") of appleseed
and it is not uncommon to refer to it as "appleseed".

To start appleseed.studio on Windows, open the `appleseed\bin` directory and double-click
on `appleseed.studio.exe`:

![On Windows, double-click on appleseed.studio.exe](/img/docs/starting-appleseed-studio-windows.png)


As the time of writing, on Linux and OS X, you will need to open a terminal, navigate to
the `appleseed/bin` directory and type:

    ./appleseed.studio

to start appleseed.studio. (We plan to make a real OS X application at some point.)

![appleseed.studio at startup](/img/docs/appleseed-studio-startup.png)

A window like the one shown above should appear.

appleseed.studio's main window is divided in four sections:

1. The **Render Area** in the middle (currently empty).
2. The **Project Explorer** on the left allows to browse the entities that make up the scene.
3. The **Attribute Editor** on the right allows to edit the properties of the selected entity.
4. The **Log Panel** at the bottom is a log of the application's activity, and will display
   info, progress, warning and error messages.

The panels can be individually docked and undocked. They can also be hidden using the buttons
at the right-bottom corner of the window.

Finally, pressing <kbd>F11</kbd> will hide all panels. Pressing <kbd>F11</kbd> again will restore them.

appleseed.studio will remember the state of the user interface when you quit and restore it
next time you open appleseed.studio.


### Loading and rendering a built-in scene

appleseed comes with a built-in Cornell Box scene that's perfect for illustrating the basics
of appleseed.studio's user interface. Load this scene by going to the **File &rsaquo; Open Built-in Project**
menu and selecting **Cornell Box**. A black square appears in the middle of the render area.
We call this the **Render Widget**.

Let's start rendering: go to the **Rendering** menu and select **Start Interactive Rendering**,
or simply press <kbd>F5</kbd>.

At first, the Cornell Box image is noisy, but the longer you let it render, the smoother it
will become. By default, interactive rendering will continue refining the image indefinitely.

![The Cornell Box in appleseed.studio](/img/docs/appleseed-studio-cornell-box.png)

You can stop rendering by selecting **Stop Rendering** in the **Rendering** menu, or by
pressing <kbd>Shift-F5</kbd>.


### Navigating in the scene

Interactive rendering must be running in order to navigate in the scene. Press <kbd>F5</kbd> to start
interactive rendering.

Let's now change the view point. The controls are as follow:

- To **rotate** the camera: **Ctrl** + **left mouse button** + drag in the render widget
- To **truck** the camera: **Ctrl** + **middle mouse button** + drag in the render widget
- To **dolly** the camera: **Ctrl** + **right mouse button** + drag in the render widget


### Starting a final render

Until now, we've only used interactive rendering. This rendering mode is suited for quick
preview, scene navigation and materials / lights tweaking, however it is suboptimal when
it comes to producing the final image of your scene. That's the role of the Final rendering
mode.

You can start final rendering of your scene by going to the **Rendering** menu and selecting
**Start Final Rendering**, or by pressing <kbd>F6</kbd>. Like for interactive rendering, you can
interrupt rendering at any point by pressing <kbd>Shift-F5</kbd>.

As you can notice, rendering proceeds in tiles. By default there are as many tiles being
rendered simultaneously as you have logical CPU cores in your machine.

Depending on the render settings, the renderer will do a single pass over the entire image,
or will progressively refine the image by doing multiple passes (but still using tiles,
unlike in interactive rendering).


### Changing the render settings

Rendering must be stopped before render settings can be changed. If you haven't done so yet,
stop rendering by pressing <kbd>Shift-F5</kbd>.

Open the **Render Settings** dialog by pressing <kbd>F7</kbd>.

![The Render Settings dialog of appleseed.studio](/img/docs/appleseed-studio-render-settings.png)

Note the **Configuration** dropdown list at the top: it allows to select which configuration
(**Final**, for the final rendering mode, or **Interactive**, for the interactive rendering
mode) to change the settings for.

Let's change the final render settings: make sure the **Final** configuration is selected, as
in the picture above.

One of the drawback of the final rendering mode, as it is configured by default, is that you
may need to wait a long time before being sure the result as a whole matches your expectations.

While you should generally make sure that everything looks good before starting a potentially
lengthly final render of your scene, there is a middle ground mode that may be of interest:
multipass final rendering. In this mode, the renderer will do multiple final render passes
over the image, with each pass reducing the amount of noise. The benefit of this approach is
to combine the efficiency of the final rendering mode with some form of progressivity.

Let's increase the number of passes (set to 1 by default) to 8. Let's also decrease the number
of samples added by each pass from 64 to 8:

![Setting up multipass rendering](/img/docs/appleseed-studio-render-settings-multipass.png)

Press **OK** to apply the changes and press <kbd>F6</kbd> to start a new final render.

With 8 passes, each adding 8 samples to every pixels, the total number of samples will be
equal but you will have an overview of the final result in 1/8<sup>th</sup> of the time.


### Closing notes

That's it for this short introduction to appleseed. We barely scratched the surface of
appleseed.studio functionalities, and we didn't cover the other tools of the appleseed
distribution, notably the command line renderer. Check out the tutorials to start
discovering and learning the deep set of functionalities offered by appleseed.
