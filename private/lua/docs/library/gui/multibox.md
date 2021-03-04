# gui.Multibox

## Syntax
```lua
gui.Multibox(parent:object, name:string)
```

## Parameters
```parent``` A gui object.

```name``` Varname of this object.

## Return value
This function returns the created GUI object.

## Example
```lua
local emb_misc = gui.Reference("MISC");
local emb_gui = gui.Tab(emb_misc, "emb_gui", "Example Multibox");


-- Creating the object
local emb_multibox = gui.Multibox(emb_gui, "The Name");

-- We will now add 2 checkboxes to the multibox
local emb_checkbox_a = gui.Checkbox(emb_multibox, "emb_checkbox_a", "this checkbox a", true)
local emb_checkbox_b = gui.Checkbox(emb_multibox, "emb_checkbox_b", "this checkbox b", false)
```

Screenshot
<figure>
  <img src="/kb/lua/docs/library/gui/multibox_ss_transparent.png"/>
</figure>
