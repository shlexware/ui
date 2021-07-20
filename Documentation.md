# ShlexLib - Version B7 Documentation


## Starting the Library
```lua
local ShlexLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/shlexsoftworks/ShlexLib/main/source"))()
```

## Creating a Window
```lua
local Window = ShlexLib:Window("Window","WindowSubtitle","LoadingText1","LoadingText2","LoadingText3","LoadingTextFinal")
```

## Creating a Tab
```lua
local Tab = Window:Tab("Tab",0000)
```

The above ``0000`` in argument 2 is an Image Decal, used for icons on the side of the Menu.

## Notifying the user
```lua
ShlexLib:Notify("NotificationTitle","NotificationContent",0000)
```

The above ``0000`` in argument 3 is an Image Decal, used for an icon in the Notification.

## Creating a Button
```lua
Tab:Button("Button", function()
   print("This button has been pressed")
end)
```

## Creating a Checkbox (toggle)
```lua
Tab:Checkbox("Checkbox", true, function(bool)
    print(bool)
end)
```

The above ``true`` in argument 2, is the default, whether the box is checked or not at the start.

## Creating a Color Picker
``This is currently not an enabled feature in the ShlexLib alpha``
```lua
Tab:ColorPicker("ColorPicker", Color3.fromRGB(255, 255, 255), function(color)
   print(color)
end)
```

## Creating a Slider
``This is currently not an enabled feature in the ShlexLib alpha``n\
No documentation

## Creating a Label
```lua
Tab:Label("Label")
```

## Creating a Paragraph
```lua
Tab:Paragraph("Paragraph","Paragraph Content")
```

## Creating an Input (TextBox)
```lua
Tab:Input("Input", function(Text)
   print(Text)
end)
```

## Creating a Dropdown menu
``This is currently not an enabled feature in the ShlexLib alpha``
```lua
local Dropdown = Tab:Dropdown("Dropdown", {"Button 1", "Button 2", "Button 3"}, function(SelectedButton)
   print(SelectedButton)
end)
```

### Adding a new button to the Dropdown
```lua
Dropdown:Button("Button")
```

### Removing an existing button from the Dropdown
```lua
Dropdown:Remove("Button")
```

## Destroying the Interface
``This is currently not an enabled feature in the ShlexLib alpha``
```lua
library:Destroy()
```