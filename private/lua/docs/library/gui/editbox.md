# gui.Editbox

## Syntax
```
gui.Editbox(parent:string, varname:string, value:string)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```title``` A string value.

## Return value
Returns a single string.


## Example
General usage
```lua
local eeb_misc = gui.Reference("MISC");
local eeb_gui = gui.Tab(eeb_misc, "eeb_gui", "Example Editbox");


-- Creating the object
local eeb_editbox = gui.Editbox(eeb_gui, "eeb_editbox", "This is the text above the box");


-- Return Example
callbacks.Register("Draw",function()
    local eeb_value = eeb_editbox:GetValue();
    print(eeb_value);
end);
```

Simple text change listener.
```lua
-- Basic setup stuff
local eeb_misc = gui.Reference("MISC");
local eeb_gui = gui.Tab(eeb_misc, "eeb_gui", "Example Editbox");


-- Creating the object
local eeb_editbox = gui.Editbox(eeb_gui, "eeb_editbox", "This is the text above the box");


-- We are gonna keep track of the last text set here
local cur_text = eeb_editbox:GetValue();


-- Return Example
callbacks.Register("Draw",function()
    -- Now to check if the text has changed
    if cur_text ~= eeb_editbox:GetValue() then
        cur_text = eeb_editbox:GetValue()
        eeb_editbox_TextChanged();
    end
end);


function eeb_editbox_TextChanged()
    -- We will now print the current text to the console
    print(cur_text);
end
```

How to set the text inside the box.
```lua
eeb_editbox:SetValue("This will be in the box");
```
