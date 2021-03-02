# Register a callback
In short terms a callback is a function that will be invoked at a specific point
in time. This will allow you to execute specific logic at the right stage.

Registering a callback is done by using ```callbacks.Register``` from the
Callbacks library.

!!! note
	Read more about the [callbacks.Register](docs/library/callbacks/register.md).

Let's say you would like to draw the current date on screen. You will require
to register a callback that will get called by our software each time is
executing the drawing logic.

```lua
local function ExampleDrawingHook()
	draw.Color( 220, 50, 50 );
	draw.Text( 128, 128, os.date() );
end

callbacks.Register( "Draw", "ExampleDrawingHook", ExampleDrawingHook );
```
