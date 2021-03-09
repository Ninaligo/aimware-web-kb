# gui.Reference
Finds and creates new reference to UI object. Should be used only once.

## Syntax
```
{guiobject} gui.Reference(string:uiobject)
```

## Parameters
```uiobject``` Object from the UI.


## Return value
Returns an guiobject.

## Example
```lua
local fvis = gui.Reference("VISUALS")
print(fvis:GetName())
--Visuals
```
