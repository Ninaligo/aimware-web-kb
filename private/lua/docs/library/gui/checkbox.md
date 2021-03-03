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
local ecb_checkbox = gui.Checkbox(ecb_gui, "ecb_checkbox", "Check me!", false);


-- Return Example
callbacks.Register("Draw", function()
local ecb_value = ecb_checkbox:GetValue();
print(ecb_value);
end);
```

Simple checkbox listener.
```lua
-- Basic setup stuff
local ecb_misc = gui.Reference("MISC");
local ecb_gui = gui.Tab(ecb_misc, "ecb_gui", "Example Checkbox");


-- Creating the object
local ecb_checkbox = gui.Checkbox(ecb_gui, "ecb_checkbox", "Check me!", false);


-- We are gonna keep track of the last value
local ecb_value = ecb_checkbox:GetValue();


-- Return Example
callbacks.Register("Draw",function()
    -- Now to check if the text has changed
    if ecb_value ~= ecb_checkbox:GetValue() then
        ecb_value = ecb_checkbox:GetValue()
        ecb_checkbox_Changed();
    end
end);


function ecb_checkbox_Changed()
    print(ecb_value);
end
```

Set the value of the checkbox
```lua
ecb_checkbox:SetValue(true);
```
