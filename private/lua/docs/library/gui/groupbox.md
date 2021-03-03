# gui.Groupbox

## Syntax
```
gui.Groupbox(parent:string, name:string, x:int, y:int, width:int, height:int)
```

## Parameters
```parent``` A gui object.

```name``` Label of object.

```x``` Integer of the horizontal axias. (Optional)

```y``` Integer of the vertical axis. (Optional)

```width``` Integer of the width. (Optional)

```height``` Integer of the height. (Optional)

## Return value
This does not return a value.


## Example
```lua
local egb_misc = gui.Reference("MISC");
local egb_gui = gui.Tab(egb_misc, "egb_gui", "Example Groupbox");


-- Creating the object
local egb_groupbox_a = gui.Groupbox(egb_gui, "Wanna be a groupie? A", 16, 16, 287.5, 50);
local egb_groupbox_b = gui.Groupbox(egb_gui, "Wanna be a groupie? B", 319.5, 16, 287.5, 100);


-- Lets add a few objects to make it look pretty
-- So we call groupbox here instead of gui so it will put it inside the gui instead
local egb_checkbox_a = gui.Checkbox(egb_groupbox_a, "egp_checkbox_a", "My checkbox groupie A", true);
local egb_checkbox_b = gui.Checkbox(egb_groupbox_b, "egp_checkbox_b", "My checkbox groupie B", true);
```
