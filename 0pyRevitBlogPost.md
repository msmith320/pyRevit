---
layout: page
title: What's pyRevit
permalink: /whatspyrevit/
---

***pyRevit*** is an IronPython script library for Revit.
However, it is not really written as an example library.
It is a working set of tools fully written in IronPython that explores the power of scripting for Revit and also adds some cool functionality.

Download and install it, launch Revit and you will note the new ***pyRevit*** tab that hosts buttons to launch all the scripts provided by the package to easily run them without the need to load them in [RevitPythonShell](https://github.com/architecture-building-systems/revitpythonshell) or some similar IronPython console.

You can also write your own scripts and add them to the tab.

There is even a Reload button than dynamically adds the new scripts to the current Revit session without the need to restart Revit.

All the scripts are provided in the `pyRevit/Extensions` folder which is downloaded at installation. You can look into them and learn how to use IronPython for Revit to perform different tasks.


## A Quick Look at some pyRevit Scripts

Let's take a quick look at some of the more useful scripts in this library:

### Selection Memory

A couple of scripts help you select object more efficiently in Revit. They are similar to the M+, M-, buttons on calculators where you can add or deduct values from memory and read the final value using the MR button.

Under the ***pyRevit*** tab, you'll find MAppend, MAppendOverwrite, MRead, MDeduct, and MClear buttons that add, add and overwrite, read, deduct, and clear the contents of the selection memory. Using these tools, you can navigate between multiple views and select objects, add them to the memory and when you're done, recall the selection. These tools work really well in combination with other selection tools under ***pyRevit*** tab. See images here for the tools and tooltips.

Each tooltip shows the button name, the script that the button is associated with and a description of what the script does.

![MAppendOverWrite](http://eirannejad.github.io/pyRevit/images/mappendoverwrite.png)
![MRead](http://eirannejad.github.io/pyRevit/images/mread.png)
![OtherMemory](http://eirannejad.github.io/pyRevit/images/othermemory.png)

### Copy and Convert Legend Views

This set of scripts help you copy Legend Views to all other project open within a Revit session.
You can copy the Legends as Legend views or as Drafting views.

![CopyLegends](http://eirannejad.github.io/pyRevit/images/copylegends.png)

Two more scripts duplicate and convert Legend views to Drafting views and vice versa within the same project.

![DuplicateLegends](http://eirannejad.github.io/pyRevit/images/convertlegends.png)

### Matching Element Graphic Overrides

This one is pretty obvious. Run the script, select your source object to pick up the style, and then one by one, select the destination objects to apply the graphic overrides. You can also navigate to other views and apply to objects within that view.

![MatchGraphicOverrides](http://eirannejad.github.io/pyRevit/images/matchgraphicoverrides.png)

***pyRevit*** provides many other powerful scripts, and most of them are really useful in a production environment.

![AnalsisAndModifyPallete](http://eirannejad.github.io/pyRevit/images/analysisandmodifypallete.png)
![ProjectPallete](http://eirannejad.github.io/pyRevit/images/projectpallete.png)
![DesktopPallete](http://eirannejad.github.io/pyRevit/images/desktoppallete.png)


## An Even Quicker but Deeper Look at Setting up pyRevit

Now let's take an even quicker and slightly deeper look at setting up [pyRevit](https://github.com/eirannejad/pyRevit):

In it's simplest form, it's a series of IronPython script bundles. Each bundle has a `script.py` and might also include an icon as `icon.png`.

![pyrevitFolder](http://eirannejad.github.io/pyRevit/images/pyrevitfolder.png)

Since Revit itself does not provide an IronPython console, you
need [RevitPythonShell](https://github.com/architecture-building-systems/revitpythonshell) to
run them.

![RPSconsole](http://eirannejad.github.io/pyRevit/images/revitpythonshellconsole.png)

Let's say you have written a script that automatically designs amazing buildings and creates the Revit model and construction documents for it, and let's say you want to run this script as fast as you can and make a whole buncha money really quickly, but it takes time to open the command prompt every time, browse to the script file, open it and run it, so you naturally want something faster!

In order to make [pyRevit](https://github.com/eirannejad/pyRevit) more user friendly, it includes a helper python library (`import pyrevit`) that finds all the other scripts and creates buttons for them in the Revit user interface. This way. you can just click on the buttons instead of using the command prompt.

What's neat about this is that the user interface buttons only store the address to each script. The script is reloaded and run every time the user clicks on the button.

This means that you can change a script on the fly while Revit is running, and the next time you click on the button, Revit will run the modified script.

If you'd like to find out more about ***pyRevit*** and how to add your own scripts, visit the [pyRevit GitHub home page](https://github.com/eirannejad/pyRevit) and everything you want to know about it is provided.

Happy scripting!
		