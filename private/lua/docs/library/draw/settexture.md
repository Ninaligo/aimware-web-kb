# draw.SetTexture
Set current drawing texture. To be used with shape drawing like draw.FilledRect Set to nil for default state.
## Syntax
``` 
{texture} draw.SetTexture(texture)
```

## Parameters
```texture``` The texture to set.

## Example
```lua
local svgData = http.Get("https://upload.wikimedia.org/wikipedia/commons/f/fd/Ghostscript_Tiger.svg");

local imgRGBA, imgWidth, imgHeight = common.RasterizeSVG(svgData);

local texture = draw.CreateTexture(imgRGBA, imgWidth, imgHeight);

callbacks.Register("Draw", function()
    draw.SetTexture(texture);
    draw.FilledRect(0, 0, imgWidth, imgHeight);
end)
```

<figure>
  <img src="/kb/lua/docs/library/draw/createtexture.png"/>
</figure>
