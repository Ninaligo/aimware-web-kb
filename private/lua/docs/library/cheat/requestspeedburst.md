# cheat.RequestSpeedBurst
Makes speed burst activate. 

!!! note
	Speed Burst has to be enabled to request speed burst.

## Syntax
```
{function} cheat.RequestSpeedBurst()
```

## Example of appending
```lua
callbacks.Register("Draw", function()
	if input.IsButtonDown(2) then
		cheat.RequestSpeedBurst();
	end
end)
```

