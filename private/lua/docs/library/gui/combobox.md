# gui.Combobox

## Syntax
```lua
gui.Combobox(parent:object, varname:string, name:string, options:string)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```name``` Label of object.

```string``` Value of the item(s).

## Return value
Return the selected index value of the item starting with 0.

## Example
```lua
local ecb_misc = gui.Reference("MISC");
local ecb_gui = gui.Tab(ecb_misc, "ecb_gui", "Example Combobox");


-- Creating the object with a single item

local ecb_combobox_a = gui.Combobox(ecb_gui, "ecb_combobox_a", "Hmmm! Pretty Items", "Item 1");


-- Creating the object with multiple item(s)

local ecb_items = {"Item1", "Item2", "Item3", "Item4"};
local ecb_combobox_b = gui.Combobox(ecb_gui, "ecb_combobox_b", "Hmmm! Pretty Items", unpack(ecb_items));

-- Return selected value
callbacks.Register("Draw", function()
    local ecb_value_a = ecb_combobox_a:GetValue();
    local ecb_value_b = ecb_combobox_b:GetValue();
    print("ecb_value_a: " .. ecb_value_a);
    print("ecb_value_b: " .. ecb_value_b);
end);
```

Simple combo box listener
```lua
local ecb_misc = gui.Reference("MISC");
local ecb_gui = gui.Tab(ecb_misc, "ecb_gui", "Example Combobox");


-- Creating the object with a single item
local ecb_combobox_a = gui.Combobox(ecb_gui, "ecb_combobox_a", "Hmmm! Pretty Items", "Item 1");


-- We are gonna keep track of the last value
local ecb_value_a = ecb_combobox_a:GetValue();


-- Creating the object with multiple item(s)
local ecb_items = {"Item1", "Item2", "Item3", "Item4"};
local ecb_combobox_b = gui.Combobox(ecb_gui, "ecb_combobox_b", "Hmmm! Pretty Items", unpack(ecb_items));


-- We are gonna keep track of the last value
local ecb_value_a = ecb_combobox_a:GetValue();


-- Return selected value
callbacks.Register("Draw", function()
    -- We are gonna check for a value and see if it has changed
	if ecb_value_a ~= ecb_combobox_a:GetValue() then
		ecb_value_a = ecb_combobox_a:GetValue();
		ecb_combobox_a_Changed();
	end
	
	
	-- We are gonna do it again for the b value!
	if ecb_value_b ~= ecb_combobox_b:GetValue() then
		ecb_value_b = ecb_combobox_b:GetValue();
		ecb_combobox_b_Changed();
	end
end);


function ecb_combobox_a_Changed()
	print(ecb_value_a);
end


function ecb_combobox_b_Changed()
	print(ecb_value_b);
end
```

How to add more items to a combobox or set new ones
```lua
-- Setting new items
-- Example 1
ecb_combobox_a:SetOptions("value1", "value2");


-- Example 2
local items = {"value1", "value2"};
ecb_combobox_a:SetOptions(unpack(items));


-- Adding items from a prior combo box is harder and requires having an array of the items you had in it. In this cause you would just add to an array and use unpack(items) like shown above.
```