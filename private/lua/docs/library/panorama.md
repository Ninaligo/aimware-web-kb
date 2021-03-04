## Functions
```string:js RunScript(js)``` Run javascript in the context of CSGO panorama UI

```lua 
local value = 100

panorama.RunScript([[
	$.Msg("Loaded Panorama Script");
	
	NewValue = ]].. value ..[[;
	NewValue += 25;
	
	GameInterfaceAPI.ConsoleCommand(`r_eyemove "${NewValue}"`);
]]);

local JSValue = client.GetConVar("r_eyemove");
print(JSValue);

--125
```Example of importing a value into lua and exporting js value to lua.