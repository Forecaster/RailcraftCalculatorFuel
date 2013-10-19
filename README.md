RailcraftCalculatorFuel
===============================

 -- Version syntax --

Version no longer needs to be the first line. It now searches for "Version=" (case sensitive) so it can be positioned anywhere, or omitted, in which case it will not display the Version: x line in the fuel list panel.

Version syntax:

Version=x

Version scheme here is arbitrary. Currently only displayed in the fuel list panel when the file is selected.
Not really important anymore since this repository will replace the fuel list changelog.
If you do make a change you can increment the existing number by one.

 -- Comment syntax --

A comment line is any line starting with //
These lines will be ignored by the parser. This can be used to have it ignore a fuel definition or to add comments or descriptions.

 -- Fuel syntax --
 
A fuel definition of which the syntax is the following:

display name;id;state;fuel value;stacksize;origin

"Display name" is what is shown in the fuel selection list, it may contain spaces.

"id" is used internally and cannot contain spaces. Has to be unique.

"state" can be either S for solid or L for fluid/liquid. It is used for filtering.

"fuel value" or heat value is pretty obvious. The easiest way to get fuel values is by using NEI by chickenbones with NEIplugins by mistaqur.

"stacksize" is how many of these items fit in a stack. It is used when calculating total fuel value from the user specified amount of items, as well as the barrel style item display in results.

"origin" should be the name of the mod the fuel is from, "vanilla" if it is a vanilla fuel. This is currently not displayed, but the ability to display origins is planned.

 -- Filename --
 
 The filename should be the railcraft version the list is based on, as opposed to the minecraft version (old format).
 
 When the first version of railcraft is officially released for a new major minecraft version (1.x) a new fuel list file should be created, trimming all but vanilla and railcraft fuels, re-adding fuels as mods update to the new minecraft version.
