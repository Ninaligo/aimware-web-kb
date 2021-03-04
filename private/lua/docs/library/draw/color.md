# draw.Color
Set the color for drawing shapes and texts.

## Syntax
```
draw.Color(r, g, b, a)
```

## Parameters
```red``` The red channel color. Max 255.

```green``` The green channel color. Max 255.

```blue``` The blue channel color. Max 255.

```alpha``` The alpha channel opacity. Max 255.

## Example
```lua
callbacks.Register("Draw", function()
	draw.Color(255, 138, 130, 255);
	draw.Text(0, 0, "TextWithColor");
end)
```