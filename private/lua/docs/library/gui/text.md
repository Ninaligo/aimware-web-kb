# gui.Text

## Syntax
```
gui.Text(parent:string, text:string)
```

## Parameters
```parent``` A gui object.

```text``` String for the text value shown.

## Return value
This does not return a value.

## Example
Creating a text object
```lua
local etxt_misc = gui.Reference("MISC");
local etxt_gui = gui.Tab(etxt_misc, "etxt_gui", "Example Text");

-- Creating the object
local etxt_text = gui.Text(etxt_gui, "Happy little text goes here. Now make sure to beat the devil out of it!");
```
