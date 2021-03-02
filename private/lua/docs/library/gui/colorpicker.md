# gui.ColorPicker

## Syntax
```lua
gui.ColorPicker(parent:object, varname:string, name:string, r:0-255, g:0-255, b:0-255, a:0-255)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Label of object.

```r``` Value of red.

```g``` Value of green.

```b``` Value of blue.

```a``` Value of alpha.

## Return value
Return 4 values between 0 and 255. They are refered to as RGBA in that order.

## Example
```lua
local ecp_misc = gui.Reference("MISC");
local ecp_gui = gui.Tab(ecp_misc, "ecp_gui", "Example Color Picker");


-- Creating the object

local ecp_colorpicker = gui.ColorPicker(ecp_gui, "ecp_colorpicker", "Pick your color!", 255, 0, 0, 255);


-- Return Example

local r, g, b, a = ecp_colorpicker:GetValue();


-- Passing into Function Examples

getColors(ecp_colorpicker);

function getColors(color)
    local r, g, b, a = color:GetValue();
end

--

getColors(ecp_colorpicker:GetValue());

function getColors(r, g, b, a)
end
```