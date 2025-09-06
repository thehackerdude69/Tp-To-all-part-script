-- This script was made by me @CampCooking12 this script was made so you can tp to all parts in a workspace instantly so if its a obby it could collect all checkpoint and all badges have fun with it 



-- This script will teleport your character to touch all parts and models in the workspace instantly
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

local function touchAllParts()
    for _, part in pairs(workspace:GetDescendants()) do
        if part:IsA("BasePart") then
            humanoidRootPart.CFrame = part.CFrame
        end
    end
end

-- made by @CampCooking13
coroutine.wrap(touchAllParts)()
