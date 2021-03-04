# draw.Text
Draw text at x, y.

## Syntax
```
draw.Text(string:text)
```

## Parameters
```string:text``` The text to draw.

## Example
```lua
callbacks.Register("Draw", function()
    draw.Color(255, 138, 130, 255);
    draw.Text(60, 60, "Text");
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/text.png"/>
</figure>