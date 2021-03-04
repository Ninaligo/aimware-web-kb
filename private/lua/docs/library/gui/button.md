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
local ebtn_button = gui.Button(ebtn_gui, "Clicky Clicky! #1", function()
        print("you clicked me! Yay! #1");
    end);


-- Creating the object using a non-embeded function
local ebtn_button = gui.Button(ebtn_gui, "Clicky Clicky! #2", button_click);


function button_click()
    print("you clicked me! Yay! #2");
end
```
