# Class: Socket

## Fields
This class has no fields.

## Functions
```Bind(ip, port)``` Bind socket to a ip:port, returns true if successful.

```SendTo(ip, port, message)``` Send a message via UDP, returns message size.

```RecvFrom(ip, port, size)``` Receives a message, returns msg, ip, port, returns nil if nothing received.

```Close()``` Closes the socket.

## Example
```lua
--Soon
```
