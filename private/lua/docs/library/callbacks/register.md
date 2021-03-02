# callbacks.Register
Register a callback.

## Syntax
```
callbacks.Register(id:string, unique:string, function)
```
```
callbacks.Register(id:string, function)
```

## Parameters
```id``` Id of callback.

```unique``` Unique name of callback.

```function``` Lua function.

## Return value
This function has no return value.

## Example
```lua
callbacks.Register("Draw", "Unique" function()
	print("Draw Callback");
end)

callbacks.Register("Draw", function()
	print("Draw Callback");
end)
```