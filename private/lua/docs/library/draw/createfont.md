# draw.CreateFont
Create a new font to draw with. Set current font for drawing. To be used with DrawText.

## Syntax
```
draw.CreateFont(string:name, int:height, int:weight(optional))
```

## Parameters
```string:name``` The font type to use.

```integer:height``` The height size that the text will be.

```integer:weight(optional)``` The amount of darkness being added. 100-900, increments of 100.


## Example
```lua
local Font = draw.CreateFont("Bahnschrift", 20, 100)

callbacks.Register("Draw", function()
    draw.SetFont(Font);
	
	draw.Color(255, 138, 130, 255);
	
	draw.Text(60, 60, "Text");
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/createfont.png"/>
</figure>

## Fontlist
For more information about the different types of fonts.
[FontList](/kb/lua/docs/library/draw/fontlist/).