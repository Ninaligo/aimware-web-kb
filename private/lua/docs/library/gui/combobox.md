# gui.Combobox

## Syntax
```lua
gui.Combobox(parent:object, varname:string, name:string, options:string)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Label of object.

```string``` Value of the item(s).

## Return value
Coming soon.

## Example
```lua
local ecb_misc = gui.Reference("MISC");
local ecb_gui = gui.Tab(ecb_misc, "ecb_gui", "Example Combobox");


-- Creating the object with a single item

local ecb_colorpicker = gui.Combobox(ecp_gui, "ecb_combobox", "Hmmm! Pretty Items", "Item 1");


-- Creating the object with multiple item(s)

local ecb_items = {"Item1", "Item2", "Item3", "Item4"};
local ecb_colorpicker = gui.Combobox(ecp_gui, "ecb_combobox", "Hmmm! Pretty Items", unpack(ecb_items));


-- Return Example

local r, g, b, a = ecp_colorpicker:GetValue();


```