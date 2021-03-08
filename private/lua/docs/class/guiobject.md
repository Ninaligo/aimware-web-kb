# Class: GuiObject

## Fields
This class has no fields.

## Functions

```GetName()``` Return name of the object.

```SetName()``` Set the name of the object. Example, button label.

```SetValue(string:varname, object:value)```Set value of the object.

```GetValue()``` Return value of the object.

```SetActive()``` Make this object active. For windows, makes the window appear or disappear.

```IsActive()``` Return boolean, true or false if visible.

```SetText(string:text)``` Set the text of the object. For gui.Text, changes the displayed text.

```SetOpenKey(keycode)``` Change the key bind to open/close gui.Window.

```SetDescription(string:text)``` Add description to created object.

```SetOptions(option1, option2, ...)``` Set options for Combobox or Listbox.

```SetPosX(integer:number)``` Set the position of X to the object. Relative to parent

```SetPosY(integer:number)``` Set the position of Y to the object. Relative to parent

```SetWidth(integer:number)``` Set the object width.

```SetHeight(integer:number)``` Set the object Height.

```SetInvisible(boolean)``` Make object invisible or visible.

```SetDisabled(boolean)``` Set object to disabled state (not clickable).

```Remove()``` Remove UI object.

```Reference(object)``` Checks for only the child objects.

```GetString()``` Returns the value as a string object.

```SetString(string:text)``` Sets the object value as a string.

```SetIcon(texture, integer:scale)``` Sets the window icon.

```Children()``` Returns a iterator for child objects.

## Example
```lua
local Tab = gui.Tab(gui.Reference("Visuals"), "ScriptTabValue", "MyScript");
local Groupbox = gui.Groupbox(tab, "Groupbox", 16, 16);

local Value, Name = Groupbox:GetValue(), Groupbox:GetName();

Groupbox:SetDescription("New Description");
Groupbox:SetDisabled(true);
Groupbox:Remove();
```

## Example of getting/setting config values
```lua
local ragebotenabled = gui.GetValue("rbot.master");
local speedburst = gui.GetValue("misc.speedburst.enable");

gui.SetValue("misc.speedburst.enable", true);
```
!!! note
	To retrieve set config values, export your confiig to clipboard and you will be able to see the values you can get/set.

## Example of reading children objects
```lua
local function PrintChildren(obj, prefix)
	print(prefix .. obj:GetName());
	for child in obj:Children() do
		PrintChildren(child, prefix .. "\t");
	end
end

PrintChildren(gui.Reference("MENU"), "");
```