# draw.CreateTexture
Create new texture to use for drawing.

## Syntax
``` 
{texture} draw.CreateTexture(rgba, int:width, int:height)
```

## Parameters
```rgba``` The color of the texture.

```integer:width``` The width of the texture.

```integer:height``` The height of the texture.


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
