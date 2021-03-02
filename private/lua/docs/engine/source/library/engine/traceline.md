# engine.TraceLine
Trace a line from src to dst using [TraceFilterSimple]().

## Syntax
```
Trace engine.TraceLine(src:Vector3, dst:Vector3, mask:integer = MASK_VISIBLE)
```

## Parameters
```src``` Source vector.

```dst``` Destination vector.

```mask``` Mask for the trace. See [trace masks]().

## Return value
The function always returns a [Trace](../../class/trace.md) that determine the result of the trace.

## Example
```lua
local src = ...;
local dst = ...;

local tr = engine.TraceLine(src, dst, 0xFFFFFFFF);

print(tr.fraction);
print(tr.entity);
print(tr.plane.normal);
```
