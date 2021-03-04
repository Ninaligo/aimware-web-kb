# Callbacks
Available callbacks inside all products marked as V5.

## DrawESP(EspBuilder)
Called for every ESP entity. Returns [EspBuilder](./class/espbuilder.md).

## DrawModel(DrawModelContext)
Called before model is drawn, eg. player or weapon model. Returns [DrawModelContext](./class/drawmodelcontext.md).

## CreateMove(UserCmd)
Called every input update, allows to modify viewangles, sendpacket, etc. Returns [UserCmd](./class/usercmd.md).

## FireGameEvent(GameEvent)
Called for selected game events. Returns [GameEvent](./class/gameevent.md).

## DispatchUserMessage(UserMessage)
Called on every user message received from server. Returns [UserMessage](./class/usermessage.md).

## SendStringCmd(StringCmd)
Called when console command is sent to server, ex. chat command "say". Returns [StringCmd](./class/stringcmd.md).

## AimbotTarget(Entity)
Called when legitbot or ragebot switches target. Returns [Entity](./class/entity.md).
