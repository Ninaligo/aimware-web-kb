# Class: File

## Fields
This class has no fields.

## Functions
```string Read()``` Read the file content.

```Write(buffer:string)``` Write inside the file.

```int Size()``` Get the file size.

```Close()``` Close the handle.

## Example
```lua
file:Write("file.txt", "1000");
local text = file:Read("file.text");
```