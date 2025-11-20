local p=game.Players.LocalPlayer
local u=game:GetService("UserInputService")

local g=Instance.new("ScreenGui",p.PlayerGui)
local t=Instance.new("TextLabel",g)
t.Size=UDim2.new(1,0,0,50)
t.Position=UDim2.new(0,0,.45,0)
t.BackgroundTransparency=1
t.Text="CRIADO POR PETERCOE"
t.TextScaled=true
t.TextColor3=Color3.new(1,1,1)
t.TextTransparency=1

for i=1,0,-.05 do t.TextTransparency=i;task.wait(.03) end
task.wait(1.2)
for i=0,1,.05 do t.TextTransparency=i;task.wait(.03) end
g:Destroy()

u.InputBegan:Connect(function(i,gp)
    if gp or not u:IsKeyDown(Enum.KeyCode.LeftShift) then return end
    local h=p.Character and p.Character:FindFirstChild("HumanoidRootPart")
    if not h then return end
    if i.KeyCode==Enum.KeyCode.One then
        h.CFrame=CFrame.new(5344,21,-474)
    elseif i.KeyCode==Enum.KeyCode.Two then
        h.CFrame=CFrame.new(4991,180,-84)
    end
end)
