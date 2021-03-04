# draw.Triangle
Draw filled triangle.

## Syntax
```
draw.Triangle(int:x1, int:y1, int:x2, int:y2, int:x3, int:y3)
```

## Parameters
```integer:x1``` First point number of x.

```integer:y1``` First point number of y.

```integer:x2``` Second point number of x.

```integer:y2``` Second point number of y.

```integer:x3``` Third point number of x.

```integer:y3``` Third point number of y.

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