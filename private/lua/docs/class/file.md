# Class: File

## Fields
This class has no fields.

## Functions
```string Read()``` Read the file content.

```Write(buffer:string)``` Write inside the file.

```int Size()``` Get the file size.

```Close()``` Close the handle.

## Example
```lua
client.AllowListener("player_death");
callbacks.Register("FireGameEvent", function(e)
    if e:GetName() == "player_death"
		local Enemy = entities.GetByUserID(e:GetInt("attacker"));
    end
end)
```