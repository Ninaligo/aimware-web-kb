# draw.RoundedRect
Draw rounded rectangle with top left point at x1, y1 and bottom right point at x2, y2 radius = radius of roundness tl = round top left corner tr = round top right corner bl = round bottom left corner br = round bottom right corner.

## Syntax
```
draw.RoundedRect(x1, y1, x2, y2, radius, tl, tr, bl, br)
```

## Parameters
```x1``` First point number of x.

```y1``` First point number of y.

```x2``` Second point number of x.

```y2``` Second point number of y.

```radius``` Amount of roundness.

```tl``` Round top left corner.

```tr``` Round top right corner.

```bl``` Round bottom left corner.

```br``` Round bottom right corner.

## Example
```lua
callbacks.Register("Draw", function()
	draw.Color(255, 138, 130, 255);
	draw.RoundedRect(20, 20, 300, 200, 50, 5, 0, 0, 5);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/roundedrect.png"/>
</figure>