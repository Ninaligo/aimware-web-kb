# Callbacks
Available callbacks inside all products marked as V5.

## Draw
Called during the drawing stage every frame. Callback returns nothing. 

## DrawESP(EspBuilder)
Called for every ESP entity. Callback returns [EspBuilder](./class/espbuilder.md "EspBuilder").

## DrawModel(DrawModelContext)
Called before model is drawn, eg. player or weapon model. Callback returns [DrawModelContext](./class/drawmodelcontext.md "DrawModelContext").

