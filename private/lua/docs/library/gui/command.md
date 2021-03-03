# gui.Command
Execute a command.

## Syntax
```
gui.Command(command:string)
```

## Parameters
```command``` String that is use to call a command.

## Return value
This function has no return value.

## Example
This command will clear the chat
```lua
gui.Command("clear");
```

This will load a script
```lua
gui.Command("lua.load <scriptname>.lua");
```
