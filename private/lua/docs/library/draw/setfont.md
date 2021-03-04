# draw.SetFont
Set current font for drawing. To be used with DrawText

## Syntax
```
draw.SetFont(string:font)
```

## Parameters
```string:font``` The font to set.


## Example
```lua
local Font = draw.CreateFont("Bahnschrift", 20, 100)

callbacks.Register("Draw", function()
    draw.SetFont(Font);
	
	draw.Color(255, 138, 130, 255);
	
	draw.Text(60, 60, "Text");
end)
```

## Fontlist
For more information about the different types of fonts.
[FontList](/kb/lua/docs/library/draw/fontlist/).