# draw.GetScreenSize
Get the size of the current screen.

## Syntax
```
{width:int, height:int} draw.GetScreenSize()
```

## Return value
```integer:width``` Width of the screen.

```integer:height``` Height of the screen.

## Example
```lua
callbacks.Register("Draw", function()
    local w, h = draw.GetScreenSize();
	
	print(w .. "x" .. h);  
	
	--1600x900
end)
```
