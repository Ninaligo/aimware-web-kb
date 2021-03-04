# draw.TextShadow
Draw text with shadow at x, y.

## Syntax
```
draw.TextShadow(string:text)
```

## Parameters
```string:text``` The text to draw.

## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(255, 138, 130, 255);
    draw.TextShadow(60, 60, "Text");
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/textshadow.png"/>
</figure>