# gui.Listbox

## Syntax
```lua
gui.Listbox(parent:object, varname:string, height:int, options:string)
```

## Parameters
```parent``` A gui object.

```varname``` Varname of this object.

```height``` Interger value for the height of the box.

```string``` Value of the item(s).

## Return value
Return the selected index value of the item starting with 0.

## Example
```lua
local elb_misc = gui.Reference("MISC");
local elb_gui = gui.Tab(elb_misc, "ecb_gui", "Example Listbox");


-- Creating the object with a single item

local elb_listbox_a = gui.Listbox(elb_gui, "elb_listbox_a", 200, "Item 1");


-- Creating the object with multiple item(s)

local elb_items = {"Item1", "Item2", "Item3", "Item4"};
local elb_listbox_b = gui.Listbox(elb_gui, "elb_listbox_b", 200, unpack(elb_items));

-- Return selected value
callbacks.Register("Draw", function()
    local elb_value_a = elb_listbox_a:GetValue();
    local elb_value_b = elb_listbox_b:GetValue();
    print("elb_value_a: " .. elb_value_a);
    print("elb_value_b: " .. elb_value_b);
end);
```

Simple listbox listener
```lua
local elb_misc = gui.Reference("MISC");
local elb_gui = gui.Tab(elb_misc, "ecb_gui", "Example Listbox");


-- Creating the object with a single item

local elb_listbox_a = gui.Listbox(elb_gui, "elb_listbox_a", 200, "Item 1");


-- We are gonna keep track of the last value
local elb_value_a = elb_listbox_a:GetValue();


-- Creating the object with multiple item(s)

local elb_items = {"Item1", "Item2", "Item3", "Item4"};
local elb_listbox_b = gui.Listbox(elb_gui, "elb_listbox_b", 200, unpack(elb_items));


-- We are gonna keep track of the last value
local elb_value_b = elb_listbox_b:GetValue();


-- Return selected value
callbacks.Register("Draw", function()
    -- We are gonna check for a value and see if it has changed
	if elb_value_a ~= elb_listbox_a:GetValue() then
		elb_value_a = elb_listbox_a:GetValue();
		elb_listbox_a_Changed();
	end
	
	
	-- We are gonna do it again for the b value!
	if elb_value_b ~= elb_listbox_b:GetValue() then
		elb_value_b = elb_listbox_b:GetValue();
		elb_listbox_b_Changed();
	end
end);


function elb_listbox_a_Changed()
	print(elb_value_a);
end


function elb_listbox_b_Changed()
	print(elb_value_b);
end
```

How to add more items to a listbox or set new ones
```lua
-- Setting new items
-- Example 1
elb_listbox_a:SetOptions("value1", "value2");


-- Example 2
local items = {"value1", "value2"};
elb_listbox_a:SetOptions(unpack(items));


-- Adding items from a prior listbox is harder and requires having an array of the items you had in it. In this cause you would just add to an array and use unpack(items) like shown above.
```