# gui.ColorPicker

## Syntax
```lua
gui.ColorPicker(parent:object, varname:string, name:string, red:0-255, green:0-255, blue:0-255, alpha:0-255)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Label of object.

```red``` Value of red.

```green``` Value of green.

```blue``` Value of blue.

```alpha``` Value of alpha.

## Return value
Return 4 values between 0 and 255. They are refered to as RGBA in that order.

## Example

General Usage
```lua
local ecp_misc = gui.Reference("MISC");
local ecp_gui = gui.Tab(ecp_misc, "ecp_gui", "Example Color Picker");


-- Creating the object
local ecp_colorpicker = gui.ColorPicker(ecp_gui, "ecp_colorpicker", "Pick your color!", 255, 0, 0, 255);


-- Return Example
local r, g, b, a = ecp_colorpicker:GetValue();


-- Passing into Function Examples
callbacks.Register("Draw", function()
    Colors_A(ecp_colorpicker);
    Colors_B(ecp_colorpicker:GetValue());
end);


function Colors_A(color)
    local r, g, b, a = color:GetValue();
    print("Colors_A - " .. "Red: " .. r .. " Green: " .. g .. " Blue: " .. b .. " Alpha: " .. a);
end


function Colors_B(r, g, b, a)
    print("Colors_B - " .. "Red: " .. r .. " Green: " .. g .. " Blue: " .. b .. " Alpha: " .. a);
end
```

Setting the value of a color picker
```lua
-- SetValue({r,g,b,a})
ecp_colorpicker:SetValue({255, 255, 255, 255});
```