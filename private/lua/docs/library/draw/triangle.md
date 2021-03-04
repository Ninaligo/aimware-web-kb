# draw.Triangle
Draw filled triangle.

## Syntax
```
draw.Triangle(x1, y1, x2, y2, x3, y3)
```

## Parameters
```x1``` First point number of x.

```y1``` First point number of y.

```x2``` Second point number of x.

```y2``` Second point number of y.

```x3``` Third point number of x.

```y3``` Third point number of y.

## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(255, 138, 130, 255);
    draw.Triangle(50, 50, 300, 200, 200, 0);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/triangle.png"/>
</figure>