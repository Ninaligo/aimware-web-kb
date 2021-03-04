# Class: Entity

## Fields
This class has no fields.

## Functions
```string GetName()``` Get the name of the entity.

```string GetModelName()``` Get the model name of the entity.

```string GetClass()``` Get the class of the entity.

```integer GetIndex()``` Get the entity index.

```integer GetTeamNumber()``` Get the entity team number.

```Vector3 GetAbsOrigin()``` Get the abs origin.

```Vector3 GetMins()``` Get mins of the entity.

```Vector3 GetMaxs()``` Get maxs of the entity.

```integer GetHealth()``` Get health of the entity.

```integer GetMaxHealth()``` Get max health of the entity.

```boolean IsPlayer()``` Returns if the entity is a player.

```boolean IsAlive()``` Returns if the entity is alive.

```boolean IsDormant()``` Returns if the entity is dormant.

```mixed GetProp(name:string)``` Returns a prop value.

!!! warning
	GetProp will fail if the prop value is not an integer, a number or a Vector3.
	Consider using GetPropBool, GetPropEntity and GetPropString for boolean, Entity and
	string types.

```SetProp(name:string, value)``` Set the value of a prop.

```number GetPropFloat(...)``` Get the value of a prop as float.

```integer GetPropInt(...)``` Get the value of a prop as int.

```boolean GetPropBool(...)``` Get the value of a prop as bool.

```string GetPropString(...)``` Get the value of a prop as string.

```Vector3 GetPropVector(...)``` Get the value of a prop as vector.

```Entity GetPropEntity(...)``` Get the value of a prop as an entity.

```SetPropFloat(number, ...)``` Set the value of a prop as float object.

```SetPropInt(integer, ...)``` Set the value of a prop as int object.

```SetPropBool(boolean, ...)``` Set the value of a prop as bool object.

```SetPropVector(vector, ...)``` Set the value of a prop as vector object.

```SetPropEntity(entity, ...)``` Set the value of a prop as entity object.

```Vector3 GetHitboxPosition(id:integer)``` Get the hitbox position of the entity.

```Vector3 GetBonePosition(id:integer)``` Get the bone position of the entity.

```integer GetWeaponID()``` Get the weapon id from the entity.

```integer GetWeaponType()``` Get the weapon type from the entity.

```Vector3 GetWeaponSpread()``` Get the weapon spread from the entity.

```number GetWeaponInaccuracy()``` Get the weapon inaccuracy from the entity.

## Example
```lua
local players = entities.FindByClass("CCSPlayer");

for i = 1, #players do
	local player = players[i];
	if player:IsAlive() then
		if player:GetTeamNumber() == 2
			local ArmorValue = player:GetProp("m_ArmorValue");
		end
	end
end
```
