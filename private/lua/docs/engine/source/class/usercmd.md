# Class: UserCmd
Class to work with the current command being sent to the server.

## Fields
```integer: commad_number```

```integer: tick_count```

```EulerAngles: viewangles```

```Vector3: aimdirection```

```number: forwardmove```

```number: sidemove```

```number: upmove```

```integer: buttons```

```integer: impulse```

```integer: weaponselect```

```integer: weaponsubtype```

```integer: random_seed```

```integer: mousedx```

```integer: mousedy```

```boolean: hasbeenpredicted```

```EulerAngles: headangles```

```Vector3: headoffset```

```boolean: sendpacket```


## Functions
```EulerAngles GetViewAngles()``` Returns the viewangles.

```SetViewAngles(angles:EulerAngles)``` Set the viewangles.

```SetSendPacket(value:boolean)``` Set the value of sendpacket.

```SetButtons(buttons:integer)``` Set the buttons.

!!! warning
	When setting a button make sure to GetButtons() first and add any additional
	button using the bitwise operator OR.

!!! note
	Read more about [Bitwise Operators](http://www.lua.org/manual/5.3/manual.html#3.4.2).

!!! note
	Check the VALVe SDK regarding the value of
	[buttons](https://github.com/ValveSoftware/source-sdk-2013/blob/master/mp/src/game/shared/in_buttons.h)

```integer GetButtons()``` Returns the buttons.

```SetForwardMove(float:number)``` Set the forwardmove value.

```GetForwardMove()``` Return the amount of forward move.

```SetSideMove(float:number)``` Move to the side, accepts float value.

```GetSideMove()``` Return the amount of side move.

```SetUpMove(float:number)``` Move up, accepts float value.

```GetUpMove()``` Return the amount of up move.

```boolean GetSendPacket()``` Return the sendpacket value.

```SetSendPacket(value:boolean)``` Set the sendpacket value.


## Example
```lua
-- Add IN_ATTACK button to the current buttons.
local buttons = cmd:GetButtons();
cmd:SetButtons(buttons | (1 << 0));
```
