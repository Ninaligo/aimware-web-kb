# draw.Line
Draw line from x1, y1 to x2, y2.

## Syntax
```
draw.Line(int:x1, int:y1, int:x2, int:y2)
```

## Parameters
```integer:x1``` First point number of x.

```integer:y1``` First point number of y.

```integer:x2``` Second point number of x.

```integer:y2``` Second point number of y.

## Example
```lua
callbacks.Register("Draw", function()
	draw.Color(255, 138, 130, 255);
	draw.Line(60, 60, 200, 90);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/line.png"/>
</figure>