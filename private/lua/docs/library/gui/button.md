# gui.Button

## Syntax
```
gui.Button(parent:string, name:string, function)
```

## Parameters
```parent``` A gui object.

```name``` Text on the button.

```function``` Lua function.

## Return value
This does not return a value.

## Example
```lua
local ebtn_misc = gui.Reference("MISC");
local ebtn_gui = gui.Tab(ebtn_misc, "ebtn_gui", "Example Button");


-- Creating the object with a function embeded

local ebtn_button = gui.Button(ecp_gui, "Clicky Clicky!", function() 
        print "you clicked me! Yay!"; 
    end);


-- Creating the object using a non-embeded function

local ebtn_button = gui.Button(ecp_gui, "Clicky Clicky!", button_click);
    
function button_click()
    print "you clicked me! Yay!"; 
end
```