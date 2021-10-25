if game.CoreGui:FindFirstChild("UILib") then
     game.CoreGui:FindFirstChild("UILib"):Destroy()
    wait()
     end
local ts = game:GetService("TweenService")
local UILib = Instance.new("ScreenGui")
UILib.Name = "UILib"
UILib.Parent = game.CoreGui
function createWindow(windowName)


     local Section = Instance.new("Frame")
     local UICorner = Instance.new("UICorner")
     local ambientShadow = Instance.new("ImageLabel")
     local UICorner_2 = Instance.new("UICorner")
     local topBar = Instance.new("Frame")
     local UICorner_3 = Instance.new("UICorner")
     local sectionTitle = Instance.new("TextLabel")
     local closeButton = Instance.new("TextButton")
     local UICorner_4 = Instance.new("UICorner")
     local tabSection = Instance.new("Frame")
     local UICorner_5 = Instance.new("UICorner")
     Section.Name = "Section"
     Section.Parent = UILib
     Section.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
     Section.BorderSizePixel = 0
     Section.ClipsDescendants = true
     Section.Position = UDim2.new(0.311881214, 0, 0.349450558, 0)
     Section.Size = UDim2.new(0.284158409, 0, 0.380219787, 0)
     UICorner.CornerRadius = UDim.new(0, 5)
     UICorner.Parent = Section
     ambientShadow.Name = "ambientShadow"
     ambientShadow.Parent = Section
     ambientShadow.AnchorPoint = Vector2.new(0.5, 0.5)
     ambientShadow.BackgroundTransparency = 1.000
     ambientShadow.BorderSizePixel = 0
     ambientShadow.Position = UDim2.new(0.498888195, 0, 0.497894794, 0)
     ambientShadow.Size = UDim2.new(1.14656925, 0, 1.19555247, 0)
     ambientShadow.ZIndex = 0
     ambientShadow.Image = "rbxassetid://1316045217"
     ambientShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
     ambientShadow.ImageTransparency = 0.800
     ambientShadow.SliceCenter = Rect.new(10, 10, 118, 118)
     UICorner_2.CornerRadius = UDim.new(0, 5)
     UICorner_2.Parent = ambientShadow
     topBar.Name = "topBar"
     topBar.Parent = Section
     topBar.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
     topBar.BorderSizePixel = 0
     topBar.Position = UDim2.new(0, 0, -0.00317463558, 0)
     topBar.Size = UDim2.new(1, 0, 0.140252337, 0)
     UICorner_3.CornerRadius = UDim.new(0, 5)
     UICorner_3.Parent = topBar
     sectionTitle.Name = "sectionTitle"
     sectionTitle.Parent = topBar
     sectionTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
     sectionTitle.BackgroundTransparency = 1.000
     sectionTitle.BorderSizePixel = 0
     sectionTitle.Position = UDim2.new(0, 0, 0.150899589, 0)
     sectionTitle.Size = UDim2.new(0.463722408, 0, 0.698200524, 0)
     sectionTitle.ZIndex = 4
     sectionTitle.Text = windowName or "window"
     sectionTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
     sectionTitle.TextScaled = true
     sectionTitle.TextSize = 14.000
     sectionTitle.TextWrapped = true
     closeButton.Name = "closeButton"
     closeButton.Parent = topBar
     closeButton.BackgroundColor3 = Color3.fromRGB(255, 170, 0)
     closeButton.BorderSizePixel = 0
     closeButton.Position = UDim2.new(0.914826393, 0, 0.150899589, 0)
     closeButton.Size = UDim2.new(0.0599369146, 0, 0.698200524, 0)
     closeButton.AutoButtonColor = false
     closeButton.Font = Enum.Font.SourceSans
     closeButton.Text = ""
     closeButton.TextColor3 = Color3.fromRGB(255, 255, 255)
     closeButton.TextScaled = true
     closeButton.TextSize = 14.000
     closeButton.TextWrapped = true
     
     UICorner_4.CornerRadius = UDim.new(0, 3)
     UICorner_4.Parent = closeButton
     
     tabSection.Name = "tabSection"
     tabSection.Parent = Section
     tabSection.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
     tabSection.BorderSizePixel = 0
     tabSection.Position = UDim2.new(0, 0, 0.0677135661, 0)
     tabSection.Size = UDim2.new(0.236933723, 0, 1.02795756, 0)

     UICorner_5.CornerRadius = UDim.new(0, 5)
     UICorner_5.Parent = tabSection
     local tabHolder = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local UIListLayout = Instance.new("UIListLayout")
tabHolder.Name = "tabHolder"
tabHolder.Parent = tabSection
tabHolder.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
tabHolder.BorderSizePixel = 0
tabHolder.Position = UDim2.new(0, 0, 0.0784011483, 0)
tabHolder.Size = UDim2.new(1.00000036, 0, 0.81201148, 0)
UICorner.CornerRadius = UDim.new(0, 5)
UICorner.Parent = tabHolder
UIListLayout.Parent = tabHolder
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 2)

closeButton.MouseButton1Click:connect(function()
UILib:Destroy()
end)
closeButton.MouseEnter:connect(function()
ts:Create(closeButton,TweenInfo.new(.2),{BackgroundColor3 = Color3.fromRGB(255, 71, 71)}):Play()
end)
closeButton.MouseLeave:connect(function()
ts:Create(closeButton,TweenInfo.new(.2),{BackgroundColor3 = Color3.fromRGB(255, 170, 0)}):Play()
end)
Section.Active = true
Section.Draggable = true
end
function createTab(tabName)
local tabFrame = Instance.new("ScrollingFrame")
local UIListLayout = Instance.new("UIListLayout")
local boolValue = Instance.new("BoolValue",tabFrame)
boolValue.Name = "isTab"
boolValue.Value = true
tabFrame.Name = tabName
tabFrame.Parent = UILib.Section
tabFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
tabFrame.CanvasSize = UDim2.new(0,0,50,0)
tabFrame.BackgroundTransparency = .3
tabFrame.BorderSizePixel = 0
tabFrame.Position = UDim2.new(0.261, 0,0.133, 0)
tabFrame.Size = UDim2.new(0.739, 0,0.867, 0)
tabFrame.Visible = false
UIListLayout.Parent = tabFrame
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 3)
local tabButton = Instance.new("TextButton")
tabButton.AutoButtonColor = false
tabButton.Name = tabName or "tabButton"
tabButton.Parent = UILib.Section.tabSection.tabHolder
tabButton.BackgroundColor3 = Color3.fromRGB(47, 47, 47)
tabButton.BorderSizePixel = 0
tabButton.Size = UDim2.new(1, 0, 0.117995456, 0)
tabButton.Font = Enum.Font.SourceSans
tabButton.Text = tabName or "tab"
tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
tabButton.TextScaled = true
tabButton.TextSize = 14.000
tabButton.TextWrapped = true
tabButton.MouseButton1Click:connect(function()
     for _, v in pairs(UILib.Section:GetDescendants()) do
if v.Name == "isTab" then
     if v.Parent.Name == tabName then
          v.Parent.Visible = true
          for i, x in pairs(v.Parent:GetDescendants()) do
               if x:IsA("TextButton") or x:IsA("TextLabel") then
          ts:Create(x,TweenInfo.new(1),{Transparency = 0}):Play() end end else  
               v.Parent.Visible = false
          for i, x in pairs(v.Parent:GetDescendants()) do
               if x:IsA("TextButton") or x:IsA("TextLabel") then
          ts:Create(x,TweenInfo.new(1),{Transparency = 1}):Play() end end
     end end end
     end)
end

function createButton(text,tabName,callback)
     local addButton = Instance.new("TextButton")
     addButton.Name = "basicButton"
     addButton.AutoButtonColor = false
     addButton.Parent = UILib.Section:FindFirstChild(tabName)
     addButton.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
     addButton.BorderSizePixel = 0
     addButton.Size = UDim2.new(0.999999523, 0, 0.002, 0)
     addButton.Font = Enum.Font.SourceSans
     addButton.TextColor3 = Color3.fromRGB(255, 255, 255)
     addButton.TextScaled = true
     addButton.TextSize = 14.000
     addButton.TextWrapped = true
     addButton.Text = text
     addButton.TextTransparency = 1
     addButton.BackgroundTransparency = 1
     addButton.MouseButton1Click:connect(function()
pcall(callback) 
ts:Create(addButton,TweenInfo.new(.2),{BackgroundColor3 = Color3.fromRGB(47, 47, 47)}):Play()
wait(.3)
ts:Create(addButton,TweenInfo.new(.2),{BackgroundColor3 = Color3.fromRGB(30, 30, 30)}):Play()

end)
end


     function createToggle(text,tabName,callback)
          local state = false
          local addToggle = Instance.new("TextButton")
          local toggleStatus = Instance.new("Frame")
          addToggle.Name = "basicToggle"
          addToggle.Parent = UILib.Section:FindFirstChild(tabName)
          addToggle.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
          addToggle.BorderSizePixel = 0
          addToggle.Position = UDim2.new(0, 0, 0.130620614, 0)
          addToggle.Size = UDim2.new(0.885235071, 0, 0.002, 0)
          addToggle.Font = Enum.Font.SourceSans
          addToggle.Text = text
          addToggle.AutoButtonColor = false
          addToggle.TextColor3 = Color3.fromRGB(255, 255, 255)
          addToggle.TextScaled = true
          addToggle.TextSize = 14.000
          addToggle.TextWrapped = true
          toggleStatus.Name = "toggleStatus"
          toggleStatus.Parent = addToggle
          toggleStatus.BackgroundColor3 = Color3.fromRGB(255, 84, 84)
          toggleStatus.BorderSizePixel = 0
          toggleStatus.Position = UDim2.new(1.00000012, 0, -9.19586626e-07, 0)
          toggleStatus.Size = UDim2.new(4, 0, 0.964255571, 0)
addToggle.MouseButton1Click:connect(function()
     game:GetService("RunService").Heartbeat:connect(function()
          if state == true then
pcall(callback) else return end end)
state = not state 
if state then
     ts:Create(toggleStatus,TweenInfo.new(.3),{BackgroundColor3 = Color3.fromRGB(86, 255, 74)}):Play()
elseif not state then
     ts:Create(toggleStatus,TweenInfo.new(.3),{BackgroundColor3 = Color3.fromRGB(255, 84, 84)}):Play()  end
end)
       
     end
