# file.Enumerate
Used for searching through the directory of files.

## Syntax
```
{files} file.Enumerate(callback(filename))
```

## Return value
Returns a callback of files.

## Example of enumerating
```lua
file.Enumerate(function(fil)
    print(fil);
	--Prints list of files.
end)
```