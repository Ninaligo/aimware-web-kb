# file.Open

## Syntax
```
file file.Open(string:filelocation, string:mode)
```

## Parameters

```string:location filename``` Directory string to file. "/folder/this.txt"

```string:char mode``` Mode to use for file. 

## Modes

```char:mode w``` Open write mode to a file. Write contents.

```char:mode r``` Open read mode to a file. Read contents.

```char:mode a``` Open append mode to a file. Add contents.

!!! note
	Writing and appending a file not yet created will be automatically created.

## Return value
Returns file object in the set mode.

## Example of writing
```lua
local fileWriteState = file.Open("write.txt", "w");

fileWriteState:Write("I wrote this.");
fileWriteState:Close();
```

## Example of reading
```lua
local fileReadState = file.Open("write.txt", "r");

local readtext = fileReadState:Read();
fileReadState:Close();

print(readtext);
--I wrote this.
```

## Example of appending
```lua
local fileAppendState = file.Open("write.txt", "a");
fileAppendState:Write("another writing");
fileAppendState:Close();

--
I wrote this.
another writing
```

