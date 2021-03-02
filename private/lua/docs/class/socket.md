# Class: Socket

## Fields
This class has no fields.

## Functions
```bool Bind(addr:string, port:int)```

Bind the socket. Returns a boolean if bound successfully.

```int SendTo(addr:string, port:int, message:string)```

Send message via UDP. Returns message size.

```mixed RecvFrom(addr:string, port:int, size:int)```

Receive data from the socket. Returns nil if nothing is received, otherwise
message, addr, port.

```Close()```

Close the connection.
