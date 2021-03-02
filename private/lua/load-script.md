# Load a script
In order to load a Lua script you have multiple options depending on the use case.

## Built-in Editor
The Lua Editor is the built-in editor inside the software.

* Copy the selected script you want to clipboard (CTRL+C).
* Open Settings tab in the Cheat Menu.
* Click **Create**.
* Click CTRL+V on Lua Editor.
* Click **Run** and **Save**.

## Your editor of choice
* Click **Open Settings Folder** from Settings->Advanced tab in the Cheat Menu.
* Make new file called `example.lua`
* Paste one of the scripts you want into the file.
* Save it then click **Refresh** under Lua Scripts list in menu.
* Select the script from list and press **Load**.

## Console
Open **CONSOLE** tab in cheat menu and then write the following:

```lua
lua.run "print('Hello from lua');"		--To run lua script directly
lua.load script.lua						--To run lua script from file
```

## Automatically
Select the script and click **Set As Autorun**.
This will set the script to be loaded automatically every time the software is
loaded.
