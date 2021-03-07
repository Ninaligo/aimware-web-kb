# Rect Animation
Example of how to make a animating rect.

## Example
```lua
local anim = {
    maxs = 300,
    mode = "wait",
    start = 0,
    speed = 0.5,
    complete = 1,
}

callbacks.Register("Draw", function()
	--Placeholder
	DrawFilledRect({0, 0, 0, 255}, {100, 100}, {300, 50})
    if anim.mode == "wait" then
        anim.maxs = 300;
        anim.start = globals.CurTime();
        anim.mode = "anim";
    else
        if anim.mode == "anim" then
            if (globals.CurTime() - anim.start) / (anim.speed * anim.complete) >= 1 then
                if anim.maxs <= 1 then
                    anim.mode = "wait";
                else
                    DrawFilledRect({50, 168, 90, 255}, {100, 100}, {anim.maxs, 50});
                    anim.maxs = anim.maxs - 1;
                end
            end
        end
    end
end)

function DrawFilledRect(color, position, size)
    draw.Color(color[1], color[2], color[3], color[4]);
    draw.FilledRect(position[1], position[2], position[1]+size[1], position[2]+size[2]);
end
```

<figure>
  <img src="/kb/lua/docs/library/draw/animationrect.gif"/>
</figure>