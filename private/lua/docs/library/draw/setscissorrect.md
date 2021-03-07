# draw.SetScissorRect
Remove excess things surrounding an area. 

## Syntax
```
draw.SetScissorRect(int:x, int:y, int:width, int:height)
```

## Parameters
```integer:x``` Axis x.

```integer:y``` Axis y.

```integer:width``` Width of scissoring.

```integer:height``` Height of scissoring.

## Example
```lua
callbacks.Register("Draw", function()
    draw.SetScissorRect(300,500,300,300);
	
	draw.Color(0,0,0,255);
    draw.FilledRect(300, 500, 600, 800);
	
	draw.Color(255,255,255,255);
	draw.FilledRect(300, 400, 400, 800);
	
	--Reset scissor area to allow seeing menu.
	draw.SetScissorRect(0,0,draw.GetScreenSize());
end)
```

<figure>
  Without Scissor Method
  <img src="/kb/lua/docs/library/draw/scissorwithout.png"/>
  With Scissor Method
  <img src="/kb/lua/docs/library/draw/scissorwith.png"/>
</figure>