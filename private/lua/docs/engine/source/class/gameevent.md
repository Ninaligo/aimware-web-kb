# Class: GameEvent

## Fields
This class has no fields.

## Functions
```GetName()``` Get the name of the game event.

```string GetString(field:string)``` Get the string from the game event.

```integer GetInt(field:string)``` Get the int from the game event.

```number GetFloat(field:string)``` Get the float from the game event.

## Example
```lua
client.AllowListener("player_death");
callbacks.Register("FireGameEvent", function(e)
    if e:GetName() == "player_death"
		local Enemy = entities.GetByUserID(e:GetInt("attacker"));
    end
end)
```
