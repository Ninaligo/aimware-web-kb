# gui.XML
Allows to create more complex UI via XML

## Syntax
```
{guiobject} gui.XML(string:xml)
```

## Parameters
```xml``` The text used for the ui creation.


## Return value
Returns an guiobject.

## Example layout via XML (test.xml)
```xml
<Window var="mymenu" name="My Menu" width="300" height="300">
	<Tab name="Tab 1">
		<Groupbox name="Options">
			<Checkbox var="enable" name="Enable" value="on">
				<ColorPicker var="clr" value="240 30 20 255"/>
			</Checkbox>
			<Slider var="factor" name="Factor" desc="Determine the factor." min="0" max="100"/>
			<Combobox var="mode" name="Mode" options=["Offensive","Defensive"]/>
		</Groupbox>
	</Tab>
	<Tab name="Tab 2">
		<Text>This tab is empty.</Text>
	</Tab>
</Window>
```

## Example loading XML
```lua
local test = gui.XML(file.Read("test.xml"));
local enable = test:Reference("enable");
local color = enable:Reference("clr");
local factor = test:Reference("factor");
local mode = test:Reference("mode");

callbacks.Register("Draw", function()
	if enable:GetValue() then
		draw.Color(color:GetValue());
		draw.Text(16, 16, "Enabled with factor " .. factor:GetValue() .. " and mode " .. mode:GetString());
	end
end)
```

<figure>
  <img src="/kb/lua/docs/library/gui/xml.png"/>
</figure>

