# Class: StringCmd

## Fields
This class has no fields.

## Functions
```string StringCmd:Get()``` Get string from an command.

```string StringCmd:Set(string:command)``` Set the command string.


## Example
```lua
callbacks.Register("SendStringCmd", function(cmd)
    -- replace "no" with "yes"
    if string.find(cmd:Get(), "say \"no\"") == 1 then
        cmd:Set("say \"yes\"");
    end
end)
```
