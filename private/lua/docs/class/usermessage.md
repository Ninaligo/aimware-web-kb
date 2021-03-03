# Class: UserMessage

## Fields
This class has no fields.

## Functions
```GetID()``` Get the id of an message.

```GetInt(index, repeatedIndex)```  Get the int from an message.

```GetFloat(index, repeatedIndex)``` Get the float from an message.

```GetString(index, repeatedIndex)``` Get the string from an message.

## Example
```lua
-- For more information about user messages look here:
-- https://github.com/SteamDatabase/Protobufs/blob/master/csgo/cstrike15_usermessages.proto

callbacks.Register("DispatchUserMessage", function()
    -- CS_UM_SayText2
    if msg:GetID() == 6 then

        -- CCSUsrMsg_SayText2.ent_idx
        local index = msg:GetInt(1);

        -- CCSUsrMsg_SayText2.params
        local message = msg:GetString(4, 1);

        local name = client.GetPlayerNameByIndex(index);

        print(name .. " says: " .. message);
    end  
end);
```
