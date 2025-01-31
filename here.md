# Welcome!
You might be confused. dont be! This GitHub repository is for Orion Library, no, I am not the owner of Orion Library, it is simply an Roblox UI Library made by someone, I was not given permission to make this repository so if your the owner and don’t want this up tell me!
# How this works.
So first, you will need to open Orion Library, you might be lazy to find Orion so here’s a link to the documentary. https://github.com/jensonhirst/Orion/blob/main/Documentation.md, now, what is the purpose for this repository? Well this helps you for how to use Orion, as for example, if you don’t know how to use buttons or stuff, this will show you exactly how to, anyways, let’s go!
# How to use Orion.
Orion UI Library, is for Roblox, obviously, but how can you use it? Well Orion is for people who wants to make hubs, script hubs, but may not have an computer to make one in Roblox studio, or lazy people who don’t feel like making their own UI, in which why a lot of people tend to only use Library’s, now, how can you use this? By having an Roblox executor you can simply run scripts, any scripts, starting from GUIS to anything really.
# How to boot the library
Booting the library is one of the most easiest things to do, firstly, go to Orion, use an program that lets you type and add lines of text, and simply put
```lua

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/jensonhirst/Orion/main/source')))()
```
In it! Start from creating a window by putting it under the line of where you have the boot Orion library code.
# Check the code and run!
Run your code in an Roblox executor, you can use the following: Xeno, Solara, Delta, ETC, now you should see it load up, as you look you will notice, that’s only the window, nothing really changed, now, for making tabs
# How to create Tabs.
Tabs, is very easy to create, by putting tabs under ur code you can create one, you can create multiple! But, tabs, is a bit different, you see, when creating tabs, you have to put all ur buttons under it, im a bit slow so trying to explain is one of the hardest things I try, plus, I’m not really an English speaker but I’m sure you don’t really care, by putting all the buttons under I mean that you can’t add multiple tabs and expect it to go into the first one, you have to first create an tab and put all ur buttons and create another tab to put all the buttons you in it in it.
# Creating Buttons.
This, is EXTREMELY easy. For making buttons, this is what activates a code on key press, let’s start from the start. As you can see, here is the code for creating a button.
```lua

Tab:AddButton({
	Name = "Button!",
	Callback = function()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]
```
When clicked, it will show a print in your console saying “button pressed”, in the print code, you can put ANY code you want, it doesn’t have to be an single print, but, something you should always be aware of is that this may sometimes break, Orion library isn’t better as what “Rayfield UI” is, with custom themes and stuff, but this whole repository isn’t about Rayfield. Simply put your button script in ur tab and baahaa! You’ve done it!
# Creating Checkboxes, Formely Toggles.
For checkboxes, we will call them Toggles, as they work the same as toggle buttons, you can skip this part but I’ll explain what a toggle is. So first, an toggle is basically like an button but WAY WAY WAY different, when you click it it will run a script but when you click again (simply de-toggling it) it will run a script, here’s an LUA if you don’t know what I’m talking about.
```lua
Tab:AddToggle({
    Name = "This is a toggle!",
    Default = false,
    Callback = function(Value)
        if Value then
            -- on
            print("A")
        else
            -- off
            print("B")
        end
    end    
})
```
Though, by using my script I made, it may not work, why? Well this was simply “fixed” by ChatGPT (I suspected that my code probably wouldn’t work.)
# Color Pickers.
A lot of people are VERY confused on how color pickers work, and I’m here to help thise “those” people. Firstly, color pickers is basically how you select an color of something, like an script for example, now, me, my self, I, personally don’t know how to use these too, but I figured it out, Create an GUI and put the code in to change whatever thing you want, here’s how to create an Color Picker.
```lua

Tab:AddColorpicker({
	Name = "Colorpicker",
	Default = Color3.fromRGB(255, 0, 0),
	Callback = function(Value)
		print(Value)
	end	  
})

--[[
Name = <string> - The name of the colorpicker.
Default = <color3> - The default value of the colorpicker.
Callback = <function> - The function of the colorpicker.
]]
```
Oh! And I forgot to mention, you can even set a Value (if you would like to), and that the color picker is EXTREMELY buggy on mobile.
```lua

ColorPicker:Set(Color3.fromRGB(255,255,255))
```
# Sliders.
Sliders 🍔 is also an confusing thing a lot of people don’t know how to use them actually, first, I’ll explain, Sliders (haha burgers) is basically setting what number of what you want that value to be, for example, you want to change ur gravity, here’s how you would do it, by putting this script
```lua
while true do
  wait(0.01)
  game.Workspace.Gravity = Value
end
```
This will set ur gravity to the sliders value, as confusing as what sliders are they are very easy to use and make…
# Creating Adaptive Inputs.
Honestly, knowing this repository is so you can learn how to use buttons and stuff, I have NO clue whatsoever what adaptive buttons are, if your wondering here’s the code for it
```lua

Tab:AddTextbox({
	Name = "Textbox",
	Default = "default box input",
	TextDisappear = true,
	Callback = function(Value)
		print(Value)
	end	  
})

--[[
Name = <string> - The name of the textbox.
Default = <string> - The default value of the textbox.
TextDisappear = <bool> - Makes the text disappear in the textbox after losing focus.
Callback = <function> - The function of the textbox.
]]
```
It’s really weird… just read the comments to get how to use it I guess.
# Creating Keybinds
Keybinds is very simple to make but sadly isn’t compatible for mobile, that’s if ur not using an keyboard script, Keybinds are basically easy too (Yes, I know I keep calling everything easy but it’s true, dude.) 
```lua

Tab:AddBind({
	Name = "Bind",
	Default = Enum.KeyCode.E,
	Hold = false,
	Callback = function()
		print("press")
	end    
})

--[[
Name = <string> - The name of the bind.
Default = <keycode> - The default value of the bind.
Hold = <bool> - Makes the bind work like: Holding the key > The bind returns true, Not holding the key > Bind returns false.
Callback = <function> - The function of the bind.
]]
```
By replacing the “E” with any key you want. If you were to press that key a code you inspired to replace print would run, you can even add an hold if you want too!

# Create an Drop-down.
As for a lot of people this is easy too, an drop-down is basically like an button, but more different, you see, when clicked, it can have multiple options and when clicked they will run an code, here’s an script!
```lua

Tab:AddDropdown({
	Name = "Dropdown",
	Default = "1",
	Options = {"1", "2"},
	Callback = function(Value)
		print(Value)
	end    
})

--[[
Name = <string> - The name of the dropdown.
Default = <string> - The default value of the dropdown.
Options = <table> - The options in the dropdown.
Callback = <function> - The function of the dropdown.
]]
```
# Things you NEED to use (One is optional, other isn’t.)
Put at end of ur script.
```lua

OrionLib:Init()
```
To destroy the interface.
```lua

OrionLib:Destroy()
```
# Hey!
Thank you for viewing my repository and taking all of ur precious time to actually read all of this (if you have), if you have any questions ask me! This is the end of the repository.
