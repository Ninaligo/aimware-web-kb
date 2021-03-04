# draw.OutlinedCircle
Draw outlined circle.

## Syntax
```
draw.OutlinedCircle(int:x, int:y, int:radius)
```

## Parameters
```integer:x``` Axis x.

```integer:y``` Axis y.

```integer:radius``` Round size.


## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(255, 138, 130, 255);
    draw.OutlinedCircle(150, 150, 100);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/outlinedcircle.png"/>
</figure>