# engine.TraceHull
Traces hull from src to dst with [TraceFilterSimple]().

## Syntax
```
Trace engine.TraceHull(src:Vector3, dst:Vector3, mins:Vector3, maxs:Vector3, mask:integer = MASK_VISIBLE)
```

## Parameters
```src``` Source vector.

```dst``` Destination vector.

```mins``` Mins vector.

```maxs``` Maxs vector.

```mask``` Mask for the trace. See [trace masks]().

## Return value
The function always returns a [Trace](../../class/trace.md) that determine the
result of the trace.
