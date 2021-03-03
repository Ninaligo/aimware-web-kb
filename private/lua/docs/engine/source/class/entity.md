# Class: Entity

## Fields
This class has no fields.

## Functions
```GetName()``` Get the name of the entity.

```GetClass()``` Get the class of the entity.

```GetIndex()``` Get the entity index.

```GetTeamNumber()``` Get the entity team number.

```GetAbsOrigin()``` Get the abs origin.

```GetMins()``` Get mins of the entity.

```GetMaxs()``` Get maxs of the entity.

```GetHealth()``` Get health of the entity.

```GetMaxHealth()``` Get max health of the entity.

```IsPlayer()``` Check if the entity is an player. 

```IsAlive()``` Check if the entity is alive. 

```GetProp(propName)``` Get the value of an prop. 

```SetProp(propName, value)``` Set the value of an prop. 

```GetPropFloat(...)``` Get the value of an prop as float. 

```GetPropInt(...)``` Get the value of an prop as int. 

```GetPropBool(...)``` Get the value of an prop as bool. 

```GetPropString(...)``` Get the value of an prop as string. 

```GetPropVector(...)``` Get the value of an prop as vector. 

```GetPropEntity(...)``` Get the value of an prop as an entity. 

```SetPropFloat(number, ...)``` Set the value of an prop as float object.

```SetPropInt(integer, ...)``` Set the value of an prop as int object.

```SetPropBool(boolean, ...)``` Set the value of an prop as bool object.

```SetPropVector(vector, ...)``` Set the value of an prop as vector object.

```SetPropEntity(entity, ...)``` Set the value of an prop as entity object.

```GetHitboxPosition(hitgroup)``` Get the hitbox position of the entity.

```GetBonePosition(boneIndex)``` Get the bone position of the entity.

```GetWeaponID()``` Get the weapon id from the entity.

```GetWeaponType()``` Get the weapon type from the entity.

```GetWeaponSpread()``` Get the weapon spread from the entity.

```GetWeaponInaccuracy()``` Get the weapon inaccuracy from the entity.

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

