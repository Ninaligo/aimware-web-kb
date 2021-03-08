# file.Write
Write contents to a file.

## Syntax
```
file.Write(string:filelocation, string:data)
```

## Parameters

```string:location filename``` Directory string to file. "/folder/this.txt"

```string:data Contents``` Contents to write to the file.

!!! note
	Writing to a file not yet created will be automatically created.

## Example of writing
```lua
file.Write("write.txt", "I wrote this.");
```
