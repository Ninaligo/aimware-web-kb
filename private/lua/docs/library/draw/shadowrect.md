# draw.ShadowRect
Draw shadow rectangle with top left point at x1, y1 and bottom right point at x2, y2.

## Syntax
```
draw.ShadowRect(int:x1, int:y1, int:x2, int:y2, int:radius)
```

## Parameters
```integer:x1``` First point number of x.

```integer:y1``` First point number of y.

```integer:x2``` Second point number of x, Changes Width.

```integer:y2``` Second point number of y, Changes Height.

```integer:radius``` Amount of shadow around the rectangle.

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