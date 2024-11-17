_G.AutoObby = true
local plr = game.Players.LocalPlayer
local rootpart = plr.Character:WaitForChild("HumanoidRootPart")
local spawn_point = game['Workspace']['Checkpoints']
local stages = plr['leaderstats']['Stage']
while  _G.AutoObby == true do
    for i,v in pairs(spawn_point:GetChildren()) do
        if v and v.Name == tostring(stages.Value + 1) then
            rootpart.CFrame = (v.CFrame * CFrame.new(0, 1, 0))
            wait(0.1)
        end
    end
end
