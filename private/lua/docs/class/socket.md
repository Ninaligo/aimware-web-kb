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

##Example
```lua
local serverIP = "127.0.0.1";
local serverPort = 1234;

local server = network.Socket("UDP");
local client = network.Socket("UDP");

if server:Bind(serverIP, serverPort) then
    print("Socket bound to port " .. serverPort);
end

local size = client:SendTo(serverIP, serverPort, "Hello!");

if size > 0 then
    print("Sent " .. size .. " bytes");
end

callbacks.Register("Draw", function()
    local msg, ip, port = server:RecvFrom("0.0.0.0", 0, 100);

    if msg then
        print("Received message from " .. ip .. ":" .. port .. ": " .. msg);
    end
end)
```
