# draw.Line
Draw line from x1, y1 to x2, y2

## Syntax
```
draw.Line(x1, y1, x2, y2)
```

## Parameters
```x1``` First point number of x.

```y1``` First point number of y.

```x2``` Second point number of x.

```y2``` Second point number of y.

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