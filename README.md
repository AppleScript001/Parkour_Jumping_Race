local Library = loadstring(game:HttpGet("https://pastebin.com/raw/KNBp0LRy"), "Coastified UI")()
repeat wait() until game:IsLoaded()
game:GetService("Players").LocalPlayer.Idled:connect(function()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)
local Window = Library:NewWindow("Parkour Jumping Race")

local Section = Window:NewSection("AutoFarm")
Section:CreateLabel("Training-Zone")
local Dropdown = Section:CreateDropdown("Select Training!", {"Zone1", "Zone2", "Zone3", "Zone4", "Zone5", "Zone6", "Zone7", "Zone8", "Zone9", "Zone10", "Zone11", "Zone12", "Vip1", "Vip2", "Vip3", "Vip4"}, 0, function(value)
    PlayerTP1 = value
end)
local Toggle = Section:CreateToggle("Auto [Train]", function(Value)
_G.Str = Value
while _G.Str do
wait(0.1)  -- Wait for 1 second before checking for enemies
    local args = {
        [1] = workspace:WaitForChild("CoreObjects"):WaitForChild("TrainingZones"):WaitForChild(PlayerTP1)
    }
    
    game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("TrainService"):WaitForChild("RF"):WaitForChild("Lift"):InvokeServer(unpack(args))
    
    end
end)
Section:CreateLabel("Race-Zone")
local Dropdown = Section:CreateDropdown("Select Race-Zone!", {"First", "Second", "Third", "Fourth"}, 0, function(value)
    PlayerTP2 = value
end)
local Toggle = Section:CreateToggle("Auto [Wins-Race]", function(Value)
_G.race = Value
while _G.race do
wait(0.1)  -- Wait for 1 second before checking for enemies
local args = {
    [1] = PlayerTP2
}

game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RaceService"):WaitForChild("RF"):WaitForChild("StartRace"):InvokeServer(unpack(args))

    end
end)
local Section = Window:NewSection("Pets")
local Dropdown = Section:CreateDropdown("Select ! Pets", {"Basic", "Spotted", "NEO", "Epic", "Cow", "Cold", "Magic", "Pixel", "Robot"}, 0, function(Value)
  Eggs = Value
end)

local Toggle = Section:CreateToggle("Auto Buy [x1]", function(Value)
  _G.pet = Value
while _G.pet do wait()
    game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("EggOpeningService"):WaitForChild("RF"):WaitForChild("Hatch"):InvokeServer("Single", Eggs)
end
end)
local Toggle = Section:CreateToggle("Auto Craft-All", function(Value)
  _G.craft = Value
while _G.craft do wait()
    game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("SizeService"):WaitForChild("RF"):WaitForChild("CraftAll"):InvokeServer()
end
end)
local Button = Section:CreateButton("Tp-Check", function(Value)
    for i,v in pairs(workspace.GameObjects.Eggs[Eggs]:GetDescendants()) do
if v.Name == "Surface" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.CFrame
end
end
end)
local Section = Window:NewSection("Extra")
local Toggle = Section:CreateToggle("Auto [Gift-All]", function(Value)
_G.gift = Value
while _G.gift do
wait(1)  -- Wait for 1 second before checking for enemies
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(1)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(2)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(3)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(4)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(5)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(6)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(7)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(8)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(9)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(10)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(11)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(12)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(13)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(14)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(15)
wait(0.1)
game:GetService("ReplicatedStorage"):WaitForChild("Packages"):WaitForChild("Knit"):WaitForChild("Services"):WaitForChild("RewardService"):WaitForChild("RF"):WaitForChild("Claim"):InvokeServer(16)
    end
end)
