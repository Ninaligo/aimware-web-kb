# gui.Window

## Syntax
```
gui.Window(varname:string, name:string, x:int, y, width:int, height:int)
```

## Parameters
```parent``` A gui object.

```text``` String for the text value shown.

## Return value
This does not return a value.

## Example
Creating a new window
```lua
local ewnd_window = gui.Window("wnd_window", "Example Window", 100, 100, 200, 400);
```

Adding a object to the window
```lua
local ewnd_window = gui.Window("ewnd_window", "Example Window", 100, 100, 200, 400);
local ewnd_checkbox = gui.Checkbox(ewnd_window, "ewnd_checkbox", "This is a checkbox", true);
```