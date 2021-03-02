# gui.Checkbox

## Syntax
```
gui.Checkbox(parent:string, varname:string, name:string, value:boolean)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Label of object.

```value``` true/false boolean.

## Return value
Returns a single value of true/false.


## Example
```lua
local ecb_misc = gui.Reference("MISC");
local ecb_gui = gui.Tab(ecb_misc, "ecb_gui", "Example Checkbox");


-- Creating the object

local ecb_checkbox = gui.Checkbox(ecp_gui, "ecb_checkbox", "Check me!", false);


-- Return Example

local check = ecb_checkbox:GetValue();
```