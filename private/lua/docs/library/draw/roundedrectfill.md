# draw.RoundedRectFill
Draw rounded filled rectangle with top left point at x1, y1 and bottom right point at x2, y2 radius = radius of roundness tl = round top left corner tr = round top right corner bl = round bottom left corner br = round bottom right corner.

## Syntax
```
draw.RoundedRectFill(int:x1, int:y1, int:x2, int:y2, int:radius, int:tl, int:tr, int:bl, int:br)
```

## Parameters
```integer:x1``` First point number of x.

```integer:y1``` First point number of y.

```integer:x2``` Second point number of x.

```integer:y2``` Second point number of y.

```integer:radius``` Amount of roundness.

```integer:tl``` Round top left corner.

```integer:tr``` Round top right corner.

```integer:bl``` Round bottom left corner.

```integer:br``` Round bottom right corner.

## Example
```lua
callbacks.Register("Draw", function()
	draw.Color(255, 138, 130, 255);
	draw.RoundedRectFill(20, 20, 300, 200, 50, 5, 0, 0, 5);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/roundedrectfill.png"/>
</figure>