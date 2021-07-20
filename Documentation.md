# ShlexLib
```lua
print("gay")
```
## Starting the Library
local ShlexLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/shlexsoftworks/ShlexLib/main/source"))()


## Creating a Window
local Window = library:Window("Window","WindowSubtitle","LoadingText1","LoadingText2","LoadingText3","LoadingTextFinal")


## Creating a Tab
local Tab = Window:Tab("Tab",0000)

The above ``0000`` in argument 2 is an Image Decal, used for icons on the side of the Menu.


## Creating a button
Tab:Button("Button", function()
   print("This button has been pressed")
end)

## Creating a checkbox (toggle)
Tab:Checkbox("Checkbox", true, function(bool)
    print(bool)
end)

The above ``true`` in argument 2, is the default, whether the box is checked or not at the start.

## Creating a color picker
``This is currently not an enabled feature in the ShlexLib alpha``
Tab:ColorPicker("ColorPicker", Color3.fromRGB(255, 255, 255), function(color)
   print(color)
end)

## Creating a slider
``This is currently not an enabled feature in the ShlexLib alpha``n\
No documentation

## Creating a label
Tab:Label("Label")

## Creating an Input (TextBox)
Tab:Input("Input", function(Text)
   print(Text)
end)

## Creating a Dropdown menu
``This is currently not an enabled feature in the ShlexLib alpha``
local Dropdown = Tab:Dropdown("Dropdown", {"Button 1", "Button 2", "Button 3"}, function(SelectedButton)
   print(SelectedButton)
end)

### Adding a new button to the Dropdown
Dropdown:Button("Button")

### Removing an existing button from the Dropdown
Dropdown:Remove("Button")

## Destroying the Interface
``This is currently not an enabled feature in the ShlexLib alpha``
library:Destroy()
