# file.Read
Read contents from a file.

## Syntax
```
{data} file.Read(string:filelocation)
```

## Parameters

```string:location filename``` Directory string to file. "/folder/this.txt"

## Return value
Returns data of the file.

## Example of reading
```lua
local data = file.Read("write.txt", "r");

print(data);
--I wrote this.
```
