# gui.Slider

## Syntax
```
Slider( parent, varname, name, value, min, max, inc )
gui.Slider(parent:string, varname:string, name:string, value:float, min:float, max:float, inc:float)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Text above the slider.

```value``` Float value of the current value.

```min``` Float value of the lowest value possible.

```max``` Float value of the largest value possible.

```inc``` Float value of the increment of movement. (Optional)

## Return value
This returns a single float value.

## Example

General Usage
```lua
local esdr_misc = gui.Reference("MISC");
local esdr_gui = gui.Tab(esdr_misc, "esdr_gui", "Example Slider");


-- Creating the object with a function embeded
local esdr_slider = gui.Slider(esdr_gui, "esdr_slider", "My happy little slider", 5.0, 0.0, 10.0, 0.01);


-- Return slider value
callbacks.Register("Draw", function()
    local esdr_value = esdr_slider:GetValue();
    print("esdr_value: " .. esdr_value);
end);
```

Simple slider listener
```lua
local esdr_misc = gui.Reference("MISC");
local esdr_gui = gui.Tab(esdr_misc, "esdr_gui", "Example Slider");


-- Creating the object with a function embeded
local esdr_slider = gui.Slider(esdr_gui, "esdr_slider", "My happy little slider", 5.0, 0.0, 10.0, 0.01);


-- We are gonna keep track of the last value
local esdr_value = esdr_slider:GetValue();


-- Return slider value
callbacks.Register("Draw", function()
    -- We are gonna check for a value and see if it has changed
	if esdr_value ~= esdr_slider:GetValue() then
		esdr_value = esdr_slider:GetValue();
		esdr_slider_Changed();
	end
end);


function esdr_slider_Changed()
	print("esdr_value: " .. esdr_value);
end
```

Set value of the slider
```lua
esdr_slider:SetValue(0.172);
```
