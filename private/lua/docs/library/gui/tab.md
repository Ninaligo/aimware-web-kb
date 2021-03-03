# gui.Tab

## Syntax
```
gui.Tab(parent:string, varname:string, name:string)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of the object.

```name``` String for the text of the tab:

## Return value
This does not return a value.

## Example
Creating a tab
```lua
-- We are setting the location of where the tab will be created
local etab_misc = gui.Reference("MISC");

-- This is creating the tab its self
local etab_gui = gui.Tab(etab_misc, "etab_gui", "Example Tab");
```

Disabling the tab with button press
```lua
-- We are setting the location of where the tab will be created
local etab_misc = gui.Reference("MISC");


-- This is creating the tab its self
local etab_gui = gui.Tab(etab_misc, "etab_gui", "Example Tab");


local etab_button = gui.Button(etab_gui, "Change Name", function()
		etab_gui:SetDisabled(true);
	end);
```