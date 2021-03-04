# draw.GetScreenSize
Get screen size.

## Syntax
```
{width:int, height:int} draw.GetTextSize(string:text)
```

## Parameters
```string:text``` The text to get the size of.

## Return value
```integer:width``` Width of the text.

```integer:height``` Height of the text.

## Example
```lua
callbacks.Register("Draw", function()
    local Tw, Th = draw.GetTextSize("The size of this text");
	
	print("Text Width - " .. Tw .. " Text Height - " .. Th);  
	
	--Text Width - 123 Text Height - 9
end)
```
