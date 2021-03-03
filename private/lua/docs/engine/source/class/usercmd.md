# Class: UserCmd


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
```SetViewAngles(pitch, yaw, roll)``` Lets you set the pitch, yaw, and roll values.

```GetViewAngles()``` Return the pitch, yaw, and roll values.

```SetSendPacket(sendpacket)``` Send a packet.

```SetButtons(buttons)``` Set the buttons of user.

```GetButtons()``` Return the set buttons of user.

```SetForwardMove(float:number)``` Move forward, accepts float value.

```GetForwardMove()``` Return the amount of forward move.

```SetSideMove(float:number)``` Move to the side, accepts float value.

```GetSideMove()``` Return the amount of side move.

```SetUpMove(float:number)``` Move up, accepts float value.

```GetUpMove()``` Return the amount of up move.


## Example
```lua
--Executes button on keycode 32 which is "V".
cmd:SetButtons(32);
```

## Keylist
For more information about key codes for setting buttons
[Keylist](/kb/lua/docs/library/input/keylist/).
