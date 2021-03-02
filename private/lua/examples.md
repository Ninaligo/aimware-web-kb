# Examples
Various examples of scripts.

## Draw system date
```lua
local function ExampleDrawingHook()
	draw.Color(220, 50, 50);
	draw.Text(128, 128, os.date());
end

callbacks.Register("Draw", "ExampleDrawingHook", ExampleDrawingHook);
```

## Snap lines ESP
```lua
local function ExampleSnapLines()
	local screenCenterX, screenH = draw.GetScreenSize();
	screenCenterX = screenCenterX * 0.5;

	draw.Color(255, 0, 0, 255);

	local players = entities.FindByClass("CCSPlayer");

	for i = 1, #players do
		local player = players[i];

		if player:IsAlive() then
			local x, y = client.WorldToScreen(player:GetAbsOrigin());

			if x ~= nil and y ~= nil then
				draw.Line(x, y, screenCenterX, screenH);
			end
		end
	end
end

callbacks.Register("Draw", "ExampleSnapLines", ExampleSnapLines);
```

## Kill Say
```lua
local Kill_String = "get owned";
local Death_String = "nice luck";

local function CHAT_KillSay(Event)

   if (Event:GetName() == "player_death") then

       local ME = client.GetLocalPlayerIndex();

       local INT_UID = Event:GetInt("userid");
       local INT_ATTACKER = Event:GetInt("attacker");

       local NAME_Victim = client.GetPlayerNameByUserID(INT_UID);
       local INDEX_Victim = client.GetPlayerIndexByUserID(INT_UID);

       local NAME_Attacker = client.GetPlayerNameByUserID(INT_ATTACKER);
       local INDEX_Attacker = client.GetPlayerIndexByUserID(INT_ATTACKER);

       if (INDEX_Attacker == ME and INDEX_Victim ~= ME) then

           client.ChatSay(" " .. tostring( Kill_String ) .. " " .. NAME_Victim);

       elseif (INDEX_Victim == ME and INDEX_Attacker ~= ME) then

           client.ChatSay(" " .. tostring(Death_String) .. " " .. NAME_Attacker);

       end

   end

end

client.AllowListener("player_death");

callbacks.Register("FireGameEvent", "AWKS", CHAT_KillSay);
```

## Auto Buy
```lua
local function autobuy(event)
   if event:GetName() == "round_prestart" then
       client.Command("buy scar20; buy deagle; buy vest; buy vesthelm; buy incgrenade; buy molotov; buy hegrenade; buy smokegrenade", true)
   end
end

client.AllowListener("round_prestart");

callbacks.Register("FireGameEvent", "autobuy", autobuy);
```

## Radio Spammer
```lua
local last_spam  = globals.TickCount()

local function RadioSpam()
   if globals.TickCount() - last_spam > 32 then
       client.Command("getout")
       last_spam = globals.TickCount()
   end
end

callbacks.Register("Draw", "RadioSpam", RadioSpam);
```
## GUI
```lua
local msc_ref = gui.Reference("MISC", "Part 1");
local msc_lua_checkbox = gui.Checkbox(msc_ref, "msc_lua_checkbox", "Lua Checkbox", false);

local wnd_luatest = gui.Window("wnd_luatest", "Lua GUI", 200, 200, 200, 400);
local lua_checkbox = gui.Checkbox(wnd_luatest, "lua_checkbox", "Checkbox", false);
local lua_slider = gui.Slider(wnd_luatest, "lua_slider", "Slider", 0, 0, 100);
local lua_keybox = gui.Keybox(wnd_luatest, "lua_keybox", "Keybox", 0);
local lua_combobox = gui.Combobox(wnd_luatest, "lua_combobox", "Combobox", "Combo1", "Combo2", "Combo3");

local lua_groupbox = gui.Groupbox(wnd_luatest, "Groupbox", 16, 200, 168, 100);
local lua_groupcheckbox = gui.Checkbox(lua_groupbox, "lua_groupcheckbox", "Group Checkbox", true);

local debugFont = draw.CreateFont("Tahoma", 60);

local function OnDraw()
    draw.SetFont(debugFont);
    if lua_checkbox:GetValue() then
        draw.Text(200, 200, "Checkbox is checked");
    end
    draw.Text(200, 300, "Slider: " .. lua_slider:GetValue());
end

callbacks.Register("Draw", "LuaGuiTest", OnDraw);
```

## Vector math
```lua
print(vector.Length(100, 100, 100));
print(vector.Add({0, 0, 0}, {100, 100, 100}));
print(vector.Add({0, 0, 0}, 100));
print(vector.Distance(0, 0, 0, 100, 100, 100));
print(vector.Distance({0, 0, 0 }, {100, 100, 100}));

local function OnDrawESP(builder)
    local ent = builder:GetEntity();
    local localply = entities.GetLocalPlayer();

    builder:AddTextTop("Distance: " .. vector.Distance({ent:GetAbsOrigin()}, {localply:GetAbsOrigin()}));
end

callbacks.Register("DrawESP", OnDrawESP);
```

## Chat message replacement
```lua
callbacks.Register("SendStringCmd", function(cmd)
    -- replace "no" with "yes"
    if string.find(cmd:Get(), "say \"no\"") == 1 then
        cmd:Set("say \"yes\"");
    end
end)
```

## Block sending regular chat messages
```lua
callbacks.Register("SendStringCmd", function(cmd)
    if string.find(cmd:Get(), "say") == 1 then
        cmd:Set(""); -- chat message wont be sent
    end
end)
```

## Chat logging
```lua
-- For more information about user messages look here:
-- https://github.com/SteamDatabase/Protobufs/blob/master/csgo/cstrike15_usermessages.proto

local function UserMessageCallback(msg)

    -- CS_UM_SayText2
    if msg:GetID() == 6 then

        -- CCSUsrMsg_SayText2.ent_idx
        local index = msg:GetInt(1);

        -- CCSUsrMsg_SayText2.params
        local message = msg:GetString(4, 1);

        local name = client.GetPlayerNameByIndex(index);

        print(name .. " says: " .. message);

    end

end

callbacks.Register("DispatchUserMessage", "UserMessageExample", UserMessageCallback);
```

## SVG drawing
```lua
local svgData = http.Get("https://upload.wikimedia.org/wikipedia/commons/f/fd/Ghostscript_Tiger.svg");

local imgRGBA, imgWidth, imgHeight = common.RasterizeSVG(svgData);

local texture = draw.CreateTexture(imgRGBA, imgWidth, imgHeight);

local function ExampleTextureDrawing()
    draw.SetTexture(texture);
    draw.FilledRect(0, 0, imgWidth, imgHeight);
end

callbacks.Register("Draw", "ExampleTextureDrawing", ExampleTextureDrawing);
```

## File writing
```lua
local f = file.Open("myfile.txt", "w");
f:Write("mydata");
f:Close();
```

## UDP client and server
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
