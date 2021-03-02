# Class: EulerAngles

## Fields
```number: x```

```number: y```

```number: z```

!!! note
	Instead of x, y and z you can also use pitch, yaw and roll.

## Functions
```Clear()``` Reset the angles to 0.

```Vector3 Forward()``` Get the forward vector of the angle.

```Vector3 Right()``` Get the right vector of the angle.

```Vector3 Up()``` Get the up vector of the angle.

```Normalize()``` Normalize the angle.

```Clamp()``` Clamp the angle.

## Example
```lua
local targetDirection = localplayer:GetAbsOrigin() - entity:GetAbsOrigin();
local targetAngles = targetDirection:Angles();
cmd.viewangles = targetAngles;
```
