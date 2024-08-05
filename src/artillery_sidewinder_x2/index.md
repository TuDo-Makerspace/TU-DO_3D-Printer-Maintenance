# Start
This is a simple guide containing all the information for setting up the Artillery Sidewinder x2 at home with the Prusa Slicer.

# Setting up the Slicer

We recommend you use the Prusa slicer for this printer. 
In the "**add / remove printer**" dialog:
1. select the option "**other FFF**"
2. select the brand "**Artillery**"
3. a new submenu, called "**Artillery FFF**" will appear under "other FFF"
4. select it and select the "**Artillery Sidewinder x1**"

It is important, that even when setting up the x2, you select the x1 in the adding process. There is not a preset option for the x2 regardless, since they share the same specs relevant for the slicer.

Depending on if you want to use bed leveling with the touch sensor on the extruder, you either use the "BL Touch" Profile, or not.

Your Artillery Sidewinder is now usable for basic 3d printing, keep reading for additional information on pausing prints and swichting filaments.

# Pausing Prints / Changing Filament midprint
The Artillery Sidewinder x2 has a small bug in the Prusa Slicer, where the extruder does not extrude additional filament, after pausing and resuming a print.

To fix that:
1. navigate to the "**Printer Settings**" menu on the top of the preview
2. select your Artillery profile of choice
3. select "**General**", scroll down to "**Advanced**" and uncheck the option "**Use relative E distances**"
4. navigate to "**Custom G-code**" and search for "**M83 ; extruder relative mode**" in the "**Start G-Code**" box (usually line 3)
5. replace the line with "M82 ; absolute mode"
6. scroll down to the entry "**before layer change G-Code**", delete everything in there

Now you can pause / resume your prints and be able to change filament midway through a print. 
