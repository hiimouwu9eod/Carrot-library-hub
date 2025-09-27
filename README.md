# Carrot-library-hub
A carrot with a roblox ui 
this ui is used for scirpts/lua code

how to setup watch me video to find out ------>


--step1: 
local carrotUI = loadstring(game:HttpGet("https://sirius.menu/rayfield"))()

-- Create main window
local carrotWindow = carrotUI:CreateWindow({
    Name = "Carrot Hub",
    LoadingTitle = "Loading Carrot Hub...",
    LoadingSubtitle = "by Oliver",
    ConfigurationSaving = {
        Enabled = true,
        FolderName = "CarrotHubConfig",
        FileName = "CarrotSettings"
    },
    Discord = {
        Enabled = false,
        Invite = "", 
        RememberJoins = true
    },
    KeySystem = false
})

-- Create a Tab
local carrotTab = carrotWindow:CreateTab("Main", 4483362458) -- icon can be any Roblox asset ID

-- Create a Section
local carrotSection = carrotTab:CreateSection("Carrot Features")

-- Add a Button
carrotTab:CreateButton({
    Name = "Click Me!",
    Callback = function()
        print("Carrot button clicked!")
    end
})

-- Add a Toggle
local carrotToggle = carrotTab:CreateToggle({
    Name = "Carrot Toggle",
    CurrentValue = false,
    Flag = "CarrotToggle",
    Callback = function(value)
        if value then
            print("Carrot toggle ON")
        else
            print("Carrot toggle OFF")
        end
    end
})

-- Add a Dropdown
local carrotDropdown = carrotTab:CreateDropdown({
    Name = "Carrot Options",
    Options = {"Option 1", "Option 2", "Option 3"},
    CurrentOption = "Option 1",
    MultipleOptions = false,
    Flag = "CarrotDropdown",
    Callback = function(option)
        print("Selected carrot option:", option)
    end
})

-- Add a TextBox
local carrotTextBox = carrotTab:CreateTextBox({
    Name = "Carrot Input",
    PlaceholderText = "Type something...",
    RemoveTextAfterFocusLost = true,
    Callback = function(text)
        print("Carrot text input:", text)
    end
})

-- Add a Slider
local carrotSlider = carrotTab:CreateSlider({
    Name = "Carrot Slider",
    Range = {0, 100},
    Increment = 1,
    Suffix = "%",
    CurrentValue = 50,
    Flag = "CarrotSlider",
    Callback = function(value)
        print("Carrot slider value:", value)
    end
})

