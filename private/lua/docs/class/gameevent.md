## Functions
```GetName()``` Get the name of the game event.

```GetString(fieldName)``` Get the string from the game event.

```GetInt(fieldName)``` Get the int from the game event.

```GetFloat(fieldName)``` Get the float from the game event.

## Example
```lua
client.AllowListener("player_death");
callbacks.Register("FireGameEvent", function(e)
    if e:GetName() == "player_death"
		local Enemy = entities.GetByUserID(e:GetInt("attacker"));
    end
end)
```
