# draw.ShadowRect
Draw shadow rectangle with top left point at x1, y1 and bottom right point at x2, y2.

## Syntax
```
draw.ShadowRect(x1, y1, x2, y2, radius)
```

## Parameters
```x1``` First point number of x.

```y1``` First point number of y.

```x2``` Second point number of x, Changes Width.

```y2``` Second point number of y, Changes Height.

```radius``` Amount of shadow around the rectangle.

## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(36, 36, 36, 255);
    draw.ShadowRect(50, 50, 300, 200, 100);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/shadowrect.png"/>
</figure>