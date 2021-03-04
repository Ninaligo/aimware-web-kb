# draw.FilledCircle
Draw filled circle.

## Syntax
```
draw.FilledCircle(x, y, radius)
```

## Parameters
```x``` Axis x.

```y``` Axis y.

```radius``` Round size.


## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(255, 138, 130, 255);
    draw.FilledCircle(150, 150, 100);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/filledcircle.png"/>
</figure>