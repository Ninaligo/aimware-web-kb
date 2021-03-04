## Functions
```Find(string:name)``` Find material by name. Return material.
	
```lua 
local material = materials.Find("particle/screenspace_fog")
print(material:GetTextureGroupName());
``` 

```Enumerate(callback(mat))``` Enumerate all loaded materials.

```lua 
materials.Enumerate(function(mat)
	print(mat);
	if string.find(mat:GetTextureGroupName(), "World") then
		mat:AlphaModulate(0.3);
	end
end)
``` 

```Create(string:name, material:vmt, string:type)``` Create custom material.

```lua 
``` 

!!! note
	To create custom materials follow the [Valve Material Type](https://developer.valvesoftware.com/wiki/Material) syntax.