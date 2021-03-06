# ShlexLib B11 - Documentation
This documentation is for the prebuild or alpha version of Shlex Library. This is currently verified to be up to date for ```ShlexLib version B11``` and below.

## Starting the Library
```lua
local ShlexLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/shlexsoftworks/ui/main/source"))()
```

Please note that the library isn't available to the public until launch; we're still working on it.

### Finding which version you're currently on
After the Library's main code launches, ShlexLib will `warn` with information on the library's version

## Creating a Window
```lua
local Window = ShlexLib:Window("Window","WindowSubtitle","LoadingText1","LoadingText2","LoadingText3","LoadingTextFinal")
```

The loading text(s), are not necessary and can be left `nil` or `false`. 

Other arguments such as `Window` and `WindowSubtitle` are also not necessary, will default to `Shlex Softworks`, `Ui Library` in that respective order.

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

If Domain X is found in-game, it will send an event to that, instead of using native notifications.

## Creating a Button
```lua
Tab:Button("Button", function()
   print("This button has been pressed")
end)
```

## Creating a Checkbox (toggle)
```lua
Tab:Checkbox("Checkbox", false, function(bool)
   while bool do wait() -- If it's true, it prints "true"
      print(bool)
   end
end)
```

The above ``false`` in argument 2, is the default, whether the box is checked or not at the start.

## Creating a Color Picker
``This is currently not an enabled feature in the ShlexLib alpha``
```lua
Tab:ColorPicker("ColorPicker", Color3.fromRGB(255, 255, 255), function(color)
   print(color)
end)
```

## Creating a Slider
```lua
Tab:Slider("Slider",1,10,"ValueName",Color3.fromRGB(55, 95, 167),function(Value)
    print(Value)
end)
```
The above ``1`` in argument 2 is the Minimum value for the slider

The above ``10`` in argument 3 is the Maximum value for the slider

The above ``ValueName`` in argument 4 is the name of the value for the slider (e.g Speed)

The above ``Color3.fromRGB(55, 95, 167)`` in argument 5 is the Color for the slider


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
```lua
library:Destroy()
```
