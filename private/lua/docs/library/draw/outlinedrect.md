# draw.OutlinedRect
Draw outlined rectangle with top left point at x1, y1 and bottom right point at x2, y2

## Syntax
```
draw.OutlinedRect(x1, y1, x2, y2)
```

## Parameters
```x1``` First point number of x.

```y1``` First point number of y.

```x2``` Second point number of x, Changes Width.

```y2``` Second point number of y, Changes Height.

## Example
```lua
callbacks.Register("Draw", function()
	draw.Color(255, 138, 130, 255);
    draw.OutlinedRect(50, 50, 300, 200);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/outlinedrect.png"/>
</figure>