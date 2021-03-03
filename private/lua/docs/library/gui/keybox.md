# gui.Keybox

## Syntax
```
gui.Keybox(parent:string, varname:string, name:string, key:int)
```

## Parameters
```parent``` A gui object.

```varname``` Label of object.

```name``` Integer of the horizontal axias. (Optional)

```key``` Integer of the vertical axis. (Optional)

## Return value
This returns a single integer value.


## Example
General Usage
```lua
local egb_misc = gui.Reference("MISC");
local ekb_gui = gui.Tab(egb_misc, "ekb_gui", "Example Keybox");

-- Creating the object
local ekb_keybox = gui.Keybox(ekb_gui, "ekb_keybox", "What key would you like", 0);


-- Return value
callbacks.Register("Draw", function()
	print(ekb_keybox:GetValue());
end)

```

Simple Keybox listener.
```lua
local egb_misc = gui.Reference("MISC");
local ekb_gui = gui.Tab(egb_misc, "ekb_gui", "Example Keybox");


-- Creating the object
local ekb_keybox = gui.Keybox(ekb_gui, "ekb_keybox", "What key would you like", 0);
local ekb_value = ekb_keybox:GetValue();


-- Return value
callbacks.Register("Draw", function()
	-- Now to check if the text has changed
	if ekb_value ~= ekb_keybox:GetValue() then
		ekb_value = ekb_keybox:GetValue();
		ekb_keybox_Changed();
	end
end)


function ekb_keybox_Changed()
	print(ekb_value);
end
```

Setting a key
```lua
ekb_keybox:SetValue(188) -- This will set the key to a comma
```

## Keylist
For more information about [key codes](\lua\docs\library\input\keylist\).