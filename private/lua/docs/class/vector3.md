# Class: Vector3

## Fields
```number: x```

```number: y```

```number: z```

## Functions
```Length()``` Get the length of an vector3. 

```LengthSqr()``` Get the length of an vector3 by squareroot.

```Length2D()``` Get the length of an vector3 by 2 dimension. 

```Length2DSqr()``` Get the length of an vector3 by 2D to the squareroot value.

```Dot(Vector3)``` Dot the vector3.

```Cross(Vector3)``` Cross the vector3.

```Clear()``` Clear out the vector3.

```Normalize()``` Normalize the vector3.

```Right()``` Get the right value from an vector3.

```Up()``` Get the up value from an vector3.

```Angles()```  Get the angles from an vector3.

## Example
```lua
local v1 = Vector3(100, 0, 0);
local v2 = Vector3(200, 0, 0);

print(v1:LengthSqr());
print(v2:Length2D());
```