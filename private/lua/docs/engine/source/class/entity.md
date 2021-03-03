# Class: Entity

## Fields
This class has no fields.

## Functions
```string GetName()``` Get the name of the entity.

```GetClass()``` Get the class of the entity.

```integer GetIndex()``` Get the entity index.

```integer GetTeamNumber()``` Get the entity team number.

```Vector3 GetAbsOrigin()``` Get the abs origin.

```Vector3 GetMins()``` Get mins of the entity.

```Vector3 GetMaxs()``` Get maxs of the entity.

```integer GetHealth()``` Get health of the entity.

```integer GetMaxHealth()``` Get max health of the entity.

```boolean IsPlayer()``` Check if the entity is an player.

```boolean IsAlive()``` Check if the entity is alive.

```GetProp(propName)``` Get the value of an prop.

```SetProp(propName, value)``` Set the value of an prop.

```number GetPropFloat(...)``` Get the value of an prop as float.

```integer GetPropInt(...)``` Get the value of an prop as int.

```boolean GetPropBool(...)``` Get the value of an prop as bool.

```string GetPropString(...)``` Get the value of an prop as string.

```Vector3 GetPropVector(...)``` Get the value of an prop as vector.

```GetPropEntity(...)``` Get the value of an prop as an entity.

```SetPropFloat(number, ...)``` Set the value of an prop as float object.

```SetPropInt(integer, ...)``` Set the value of an prop as int object.

```SetPropBool(boolean, ...)``` Set the value of an prop as bool object.

```SetPropVector(vector, ...)``` Set the value of an prop as vector object.

```SetPropEntity(entity, ...)``` Set the value of an prop as entity object.

```GetHitboxPosition(hitgroup)``` Get the hitbox position of the entity.

```GetBonePosition(boneIndex)``` Get the bone position of the entity.

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
