## Functions
```FindByClass(className)``` Find and put into table all entities with given class name.

```lua
--Returns table of all players
local Players = entities.FindByClass("CCSPlayer");
```

```GetLocalPlayer()```  Return the local player entity.

```lua
local LocalPlayer = entities.GetLocalPlayer();
```

```GetByIndex(index)``` Return the entity by index.

```lua
local RandomPlayer = entities.GetByIndex(3);
```

```GetByUserID(userID)``` Return the entity by user id

```lua
for i = 1, globals.MaxClients(), 1 do
	local Player = entities.GetByUserID(i);
end
```

```GetPlayerResources()``` Return the player resources entity

```lua
local PlayerResources = entities.GetPlayerResources();
```
