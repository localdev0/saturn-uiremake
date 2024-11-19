## Get Stuff
```lua
local lib = {}
local Theme = Color3.fromRGB(232, 46, 46)
local plr = game:GetService("Players").LocalPlayer

function lib:CreateWindow(title)
	local UI = Instance.new("ScreenGui")
	local Main = Instance.new("Frame")
	local SideBar = Instance.new("Frame")
	local Title = Instance.new("TextLabel")
	local UICorner = Instance.new("UICorner")
	local Navigation = Instance.new("ScrollingFrame")
	local UIListLayout = Instance.new("UIListLayout")
	local Line = Instance.new("Frame")
	local UICorner_6 = Instance.new("UICorner")
	local JustABar = Instance.new("Frame")
	local UICorner_7 = Instance.new("UICorner")
	local Subtitle = Instance.new("TextLabel")
	local Welcome = Instance.new("TextLabel")
	local IdkBar = Instance.new("Frame")
	local Line_2 = Instance.new("Frame")
	local Content = Instance.new("Frame")
	
	UI.Name = "UI"
	UI.Parent = game:GetService("Players").LocalPlayer.PlayerGui or game:GetService("CoreGui")
	UI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	UI.DisplayOrder = 99
	UI.ResetOnSpawn = false

	Main.Name = "Main"
	Main.Parent = UI
	Main.BackgroundColor3 = Color3.fromRGB(14, 14, 14)
	Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0, 350, 0, 75)
	Main.Size = UDim2.new(0, 542, 0, 384)
	
local UserInputService = game:GetService("UserInputService")

local isVisible = true

-- Function to handle Left CTRL key press
local function onInputBegan(input, gameProcessedEvent)
    if gameProcessedEvent then return end

    if input.UserInputType == Enum.UserInputType.Keyboard and input.KeyCode == Enum.KeyCode.LeftControl then
        isVisible = not isVisible
        Main.Visible = isVisible
    end
end

UserInputService.InputBegan:Connect(onInputBegan)


	SideBar.Name = "SideBar"
	SideBar.Parent = Main
	SideBar.BackgroundColor3 = Color3.fromRGB(11, 11, 11)
	SideBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	SideBar.BorderSizePixel = 0
	SideBar.Position = UDim2.new(0, 0, 3.9736431e-08, 0)
	SideBar.Size = UDim2.new(0, 155, 0, 383)

	Title.Name = "Title"
	Title.Parent = SideBar
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.0838709697, 0, 0, 0)
	Title.Size = UDim2.new(0, 142, 0, 33)
	Title.Font = Enum.Font.SourceSans
	Title.Text = title
	Title.TextColor3 = Color3.fromRGB(153, 153, 153)
	Title.TextSize = 16.000
	Title.TextTransparency = 0
	Title.TextXAlignment = Enum.TextXAlignment.Left
	
	local currentMonth = os.date("*t").month

	if currentMonth == 12 then
		Title.Text = title .. " 🎁"  -- December: Gift emoji
	elseif currentMonth == 10 or 11 then
		Title.Text = title .. " 🎃"  -- October: Pumpkin emoji
	elseif currentMonth == 7 or 8 then
		Title.Text = title .. " 🎇"  -- July: Fireworks emoji
	else
		Title.Text = title  -- Default title for other months
	end

	UICorner.Parent = SideBar

	Navigation.Name = "Navigation"
	Navigation.Parent = SideBar
	Navigation.Active = true
	Navigation.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Navigation.BackgroundTransparency = 1.000
	Navigation.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.BorderSizePixel = 0
	Navigation.Position = UDim2.new(0, 0, 0.107049607, 0)
	Navigation.Size = UDim2.new(0, 155, 0, 342)
	Navigation.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.CanvasSize = UDim2.new(0, 0, 10, 0)
	Navigation.ScrollBarThickness = 0

	UIListLayout.Parent = Navigation
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.Padding = UDim.new(0, 4)
	
	Line.Name = "Line"
	Line.Parent = Main
	Line.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line.BackgroundTransparency = 0.500
	Line.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line.BorderSizePixel = 0
	Line.Position = UDim2.new(0.285046458, 0, 0, 0)
	Line.Size = UDim2.new(0, 1, 0, 384)

	UICorner_6.Parent = Main

	JustABar.Name = "JustABar"
	JustABar.Parent = Main
	JustABar.BackgroundColor3 = Color3.fromRGB(23, 23, 23)
	JustABar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	JustABar.BorderSizePixel = 0
	JustABar.Position = UDim2.new(0, 0, 0.942708313, 0)
	JustABar.Size = UDim2.new(0, 542, 0, 22)

	UICorner_7.CornerRadius = UDim.new(0, 6)
	UICorner_7.Parent = JustABar

	Subtitle.Name = "Subtitle"
	Subtitle.Parent = JustABar
	Subtitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Subtitle.BackgroundTransparency = 1.000
	Subtitle.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Subtitle.BorderSizePixel = 0
	Subtitle.Position = UDim2.new(0.0219754297, 0, -0.272727281, 0)
	Subtitle.Size = UDim2.new(0, 142, 0, 33)
	Subtitle.Font = Enum.Font.SourceSans
	Subtitle.Text = title
	Subtitle.TextColor3 = Color3.fromRGB(255, 255, 255)
	Subtitle.TextSize = 14.000
	Subtitle.TextTransparency = 0.600
	Subtitle.TextXAlignment = Enum.TextXAlignment.Left

	Welcome.Name = "Welcome"
	Welcome.Parent = JustABar
	Welcome.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Welcome.BackgroundTransparency = 1.000
	Welcome.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Welcome.BorderSizePixel = 0
	Welcome.Position = UDim2.new(0.724103153, 0, -0.272727281, 0)
	Welcome.Size = UDim2.new(0, 142, 0, 33)
	Welcome.Font = Enum.Font.SourceSans
	Welcome.Text = "Welcome, "..plr.Name
	Welcome.TextColor3 = Theme
	Welcome.TextSize = 14.000
	Welcome.TextXAlignment = Enum.TextXAlignment.Left

	IdkBar.Name = "IdkBar"
	IdkBar.Parent = Main
	IdkBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	IdkBar.BackgroundTransparency = 1.000
	IdkBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	IdkBar.BorderSizePixel = 0
	IdkBar.Position = UDim2.new(0.28689158, 0, 0, 0)
	IdkBar.Size = UDim2.new(0, 386, 0, 55)

	Line_2.Name = "Line"
	Line_2.Parent = Main
	Line_2.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
	Line_2.BackgroundTransparency = 0.500
	Line_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line_2.BorderSizePixel = 0
	Line_2.Position = UDim2.new(0.28689158, 0, 0.143229172, 0)
	Line_2.Size = UDim2.new(0, 386, 0, 1)

	Content.Name = "Content"
	Content.Parent = Main
	Content.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Content.BackgroundTransparency = 1.000
	Content.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Content.BorderSizePixel = 0
	Content.Position = UDim2.new(0.28597787, 0, 0.145833328, 0)
	Content.Size = UDim2.new(0, 386, 0, 306)
	
	local function FXWHN_script() -- Main.dragWindow 
		local script = Instance.new('LocalScript', Main)

		local TweenService = game:GetService("TweenService")
		local UserInputService = game:GetService("UserInputService")

		local gui = script.Parent

		local dragging
		local dragInput
		local dragStart
		local startPos

		local tweenInfo = TweenInfo.new(0.16, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)

		local function update(input)
			local delta = input.Position - dragStart
			local targetPos = UDim2.new(
				startPos.X.Scale, 
				startPos.X.Offset + delta.X, 
				startPos.Y.Scale, 
				startPos.Y.Offset + delta.Y
			)

			local tween = TweenService:Create(gui, tweenInfo, {Position = targetPos})
			tween:Play()
		end

		gui.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				dragging = true
				dragStart = input.Position
				startPos = gui.Position

				-- Listen for input state change to end dragging
				input.Changed:Connect(function()
					if input.UserInputState == Enum.UserInputState.End then
						dragging = false
					end
				end)
			end
		end)

		gui.InputChanged:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				dragInput = input
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if input == dragInput and dragging then
				update(input)
			end
		end)

	end
	coroutine.wrap(FXWHN_script)()
	
	function lib:CreateTab(title)
		local Tab = {}

		local TabButton = Instance.new("TextButton")
		local TitleLabel = Instance.new("TextLabel")
		local UICorner_4 = Instance.new("UICorner")
		local ActiveLine = Instance.new("Frame")
		local UICorner_5 = Instance.new("UICorner")
		local Items = Instance.new("ScrollingFrame")
		local UIListLayout_2 = Instance.new("UIListLayout")

		TabButton.Name = "Tab"
		TabButton.Parent = Navigation
		TabButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TabButton.BackgroundTransparency = 1.000
		TabButton.BorderSizePixel = 0
		TabButton.Position = UDim2.new(0.0258064512, 0, 0, 0)
		TabButton.Size = UDim2.new(0, 147, 0, 30)
		TabButton.AutoButtonColor = false
		TabButton.Font = Enum.Font.SourceSans
		TabButton.Text = ""
		TabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
		TabButton.TextSize = 14.000

		TitleLabel.Name = "Title"
		TitleLabel.Parent = TabButton
		TitleLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TitleLabel.BackgroundTransparency = 1.000
		TitleLabel.BorderSizePixel = 0
		TitleLabel.Position = UDim2.new(0.0838710219, 0, 0, 0)
		TitleLabel.Size = UDim2.new(0, 134, 0, 28)
		TitleLabel.Font = Enum.Font.SourceSans
		TitleLabel.Text = title
		TitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
		TitleLabel.TextSize = 18.000
		TitleLabel.TextTransparency = 0.600
		TitleLabel.TextXAlignment = Enum.TextXAlignment.Left

		UICorner_4.CornerRadius = UDim.new(0, 6)
		UICorner_4.Parent = TabButton

		ActiveLine.Name = "ActiveLine"
		ActiveLine.Parent = TabButton
		ActiveLine.BackgroundColor3 = Theme
		ActiveLine.BackgroundTransparency = 1.000
		ActiveLine.BorderSizePixel = 0
		ActiveLine.Position = UDim2.new(0, 0, 0.244, 0)
		ActiveLine.Size = UDim2.new(0, 4, 0, 15)

		UICorner_5.Parent = ActiveLine

		Items.Name = title
		Items.Parent = Content
		Items.Active = true
		Items.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Items.BackgroundTransparency = 1.000
		Items.BorderSizePixel = 0
		Items.Size = UDim2.new(0, 387, 0, 306)
		Items.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
		Items.CanvasSize = UDim2.new(0, 0, 25, 0)
		Items.ScrollBarThickness = 0
		Items.Visible = false

		UIListLayout_2.Parent = Items
		UIListLayout_2.HorizontalAlignment = Enum.HorizontalAlignment.Center
		UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
		UIListLayout_2.Padding = UDim.new(0, 4)

		TabButton.MouseButton1Click:Connect(function()
			for _, otherTab in pairs(Navigation:GetChildren()) do
				if otherTab.Name == "Tab" then
					otherTab.Title.TextTransparency = 0.6
					otherTab.ActiveLine.Size = UDim2.new(0, 4, 0, 15)
					otherTab.ActiveLine.BackgroundTransparency = 1
					local otherTabItems = Content:FindFirstChild(otherTab.Title.Text)
					if otherTabItems then
						otherTabItems.Visible = false
					end
					game:GetService("TweenService"):Create(otherTab, TweenInfo.new(0.3), {BackgroundTransparency = 1}):Play()
					game:GetService("TweenService"):Create(otherTab.ActiveLine, TweenInfo.new(0.3), {Size = UDim2.new(0, 4, 0, 15)}):Play()
				end
			end

			TabButton.BackgroundTransparency = 0.95
			TitleLabel.TextTransparency = 0
			ActiveLine.Size = UDim2.new(0, 4, 0, 19)
			ActiveLine.BackgroundTransparency = 0

			Items.Visible = true

			game:GetService("TweenService"):Create(TabButton, TweenInfo.new(0.3), {BackgroundTransparency = 0.95}):Play()
			game:GetService("TweenService"):Create(ActiveLine, TweenInfo.new(0.3), {Size = UDim2.new(0, 4, 0, 19)}):Play()
		end)

		return TabButton, Items
		
	end
	
	function lib:CreateSection(title, TabParent)
		local Section = Instance.new("TextLabel")
		
		Section.Name = "Section"
		Section.Parent = TabParent
		Section.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Section.BackgroundTransparency = 1.000
		Section.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Section.BorderSizePixel = 0
		Section.Position = UDim2.new(0.31653747, 0, 0, 0)
		Section.Size = UDim2.new(0, 367, 0, 33)
		Section.Text = title
		Section.TextColor3 = Color3.fromRGB(255, 255, 255)
		Section.TextSize = 10.000
		Section.TextTransparency = 0.600
		Section.TextXAlignment = Enum.TextXAlignment.Left
	end
	
	function lib:CreateButton(title, TabParent, callback)
		local Button = Instance.new("ImageButton")
		local UICorner_14 = Instance.new("UICorner")
		local Title_6 = Instance.new("TextLabel")
		local MouseIcon = Instance.new("ImageLabel")

		Button.Name = "Button"
		Button.Parent = TabParent
		Button.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Button.BackgroundTransparency = 0.500
		Button.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Button.BorderSizePixel = 0
		Button.Position = UDim2.new(0.0271317828, 0, 0.120915033, 0)
		Button.Size = UDim2.new(0, 366, 0, 37)
		Button.AutoButtonColor = false

		UICorner_14.Parent = Button

		Title_6.Name = "Title"
		Title_6.Parent = Button
		Title_6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.BackgroundTransparency = 1.000
		Title_6.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_6.BorderSizePixel = 0
		Title_6.Position = UDim2.new(0.0292261671, 0, 0.108107693, 0)
		Title_6.Size = UDim2.new(0, 134, 0, 28)
		Title_6.Font = Enum.Font.SourceSans
		Title_6.Text = title
		Title_6.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.TextSize = 18.000
		Title_6.TextTransparency = 0.600
		Title_6.TextXAlignment = Enum.TextXAlignment.Left

		MouseIcon.Name = "MouseIcon"
		MouseIcon.Parent = Button
		MouseIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		MouseIcon.BackgroundTransparency = 1.000
		MouseIcon.BorderColor3 = Color3.fromRGB(0, 0, 0)
		MouseIcon.BorderSizePixel = 0
		MouseIcon.Position = UDim2.new(0.915300548, 0, 0.189189196, 0)
		MouseIcon.Size = UDim2.new(0, 20, 0, 19)
		MouseIcon.Image = "rbxassetid://12804017021"
		MouseIcon.ImageColor3 = Theme

		Button.MouseButton1Click:Connect(function()
			if callback then
				callback()
			end
		end)
	end
	
	local TweenService = game:GetService("TweenService")

	function lib:CreateToggle(title, TabParent, callback)
		local Toggle = Instance.new("ImageButton")
		local UICorner_8 = Instance.new("UICorner")
		local Title_4 = Instance.new("TextLabel")
		local Slide = Instance.new("Frame")
		local UICorner_9 = Instance.new("UICorner")
		local Wheel = Instance.new("Frame")
		local UICorner_10 = Instance.new("UICorner")

		Toggle.Name = "Toggle"
		Toggle.Parent = TabParent
		Toggle.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Toggle.BackgroundTransparency = 0.500
		Toggle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Toggle.BorderSizePixel = 0
		Toggle.Position = UDim2.new(0.0271317828, 0, 0.120915033, 0)
		Toggle.Size = UDim2.new(0, 366, 0, 37)
		Toggle.AutoButtonColor = false

		UICorner_8.Parent = Toggle

		Title_4.Name = "Title"
		Title_4.Parent = Toggle
		Title_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.BackgroundTransparency = 1.000
		Title_4.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_4.BorderSizePixel = 0
		Title_4.Position = UDim2.new(0.0292261671, 0, 0.108107693, 0)
		Title_4.Size = UDim2.new(0, 134, 0, 28)
		Title_4.Font = Enum.Font.SourceSans
		Title_4.Text = title
		Title_4.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.TextSize = 18.000
		Title_4.TextTransparency = 0.600
		Title_4.TextXAlignment = Enum.TextXAlignment.Left

		Slide.Name = "Slide"
		Slide.Parent = Toggle
		Slide.BackgroundColor3 = Color3.fromRGB(21, 21, 21)
		Slide.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slide.BorderSizePixel = 0
		Slide.Position = UDim2.new(0.841530025, 0, 0.351351351, 0)
		Slide.Size = UDim2.new(0, 39, 0, 12)

		UICorner_9.CornerRadius = UDim.new(1, 0)
		UICorner_9.Parent = Slide

		Wheel.Name = "Wheel"
		Wheel.Parent = Slide
		Wheel.BackgroundColor3 = Color3.fromRGB(51, 51, 51)
		Wheel.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Wheel.BorderSizePixel = 0
		Wheel.Position = UDim2.new(0, 0, -0.25, 0)
		Wheel.Size = UDim2.new(0, 19, 0, 18)

		UICorner_10.CornerRadius = UDim.new(1, 0)
		UICorner_10.Parent = Wheel

		Toggle.MouseButton1Click:Connect(function()
			local isOn = Wheel.Position == UDim2.new(0, 0, -0.25, 0)
			if isOn then
				local tweenTitle = TweenService:Create(Title_4, TweenInfo.new(0.2), {TextTransparency = 0})
				local tweenWheel = TweenService:Create(Wheel, TweenInfo.new(0.2), {Position = UDim2.new(0.512820542, 0, -0.25, 0), BackgroundColor3 = Theme})
				tweenTitle:Play()
				tweenWheel:Play()
			else
				local tweenTitle = TweenService:Create(Title_4, TweenInfo.new(0.2), {TextTransparency = 0.6})
				local tweenWheel = TweenService:Create(Wheel, TweenInfo.new(0.2), {Position = UDim2.new(0, 0, -0.25, 0), BackgroundColor3 = Color3.fromRGB(51, 51, 51)})
				tweenTitle:Play()
				tweenWheel:Play()
			end
			callback(not isOn)
		end)
	end
	
	function lib:CreateSlider(title, TabParent, min, max, callback)
		local Slider = Instance.new("ImageButton")
		local UICorner_15 = Instance.new("UICorner")
		local Title_7 = Instance.new("TextLabel")
		local SliderBack = Instance.new("Frame")
		local Draggable = Instance.new("Frame")
		local Value = Instance.new("TextLabel")

		Slider.Name = "Slider"
		Slider.Parent = TabParent
		Slider.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BackgroundTransparency = 0.500
		Slider.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BorderSizePixel = 0
		Slider.Position = UDim2.new(0.0271317828, 0, 0.522875845, 0)
		Slider.Size = UDim2.new(0, 366, 0, 39)
		Slider.AutoButtonColor = false

		UICorner_15.Parent = Slider

		Title_7.Name = "Title"
		Title_7.Parent = Slider
		Title_7.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_7.BackgroundTransparency = 1.000
		Title_7.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_7.BorderSizePixel = 0
		Title_7.Position = UDim2.new(0.0292261671, 0, -0.0195520278, 0)
		Title_7.Size = UDim2.new(0, 134, 0, 28)
		Title_7.Font = Enum.Font.SourceSans
		Title_7.Text = title
		Title_7.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_7.TextSize = 17.000
		Title_7.TextTransparency = 0.600
		Title_7.TextXAlignment = Enum.TextXAlignment.Left

		SliderBack.Name = "SliderBack"
		SliderBack.Parent = Slider
		SliderBack.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		SliderBack.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SliderBack.BorderSizePixel = 0
		SliderBack.Position = UDim2.new(0.0273224041, 0, 0.702127635, 0)
		SliderBack.Size = UDim2.new(0, 345, 0, 2)

		Draggable.Name = "Draggable"
		Draggable.Parent = SliderBack
		Draggable.BackgroundColor3 = Theme
		Draggable.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Draggable.BorderSizePixel = 0
		Draggable.Size = UDim2.new(0, 257, 0, 2)

		Value.Name = "Value"
		Value.Parent = Slider
		Value.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Value.BackgroundTransparency = 1.000
		Value.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Value.BorderSizePixel = 0
		Value.Position = UDim2.new(0.800546467, 0, -0.0195520278, 0)
		Value.Size = UDim2.new(0, 48, 0, 28)
		Value.Font = Enum.Font.SourceSans
		Value.Text = "0.1"
		Value.TextColor3 = Color3.fromRGB(255, 255, 255)
		Value.TextSize = 16.000
		Value.TextTransparency = 0.600
		Value.TextWrapped = true
		Value.TextXAlignment = Enum.TextXAlignment.Right

		local currentValue = min
		local isDragging = false
		local touchID = nil
		local UIS = game:GetService("UserInputService")
		local TweenService = game:GetService("TweenService")
		local tweenInfo = TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut)

		local function UpdateTransparency()
			if isDragging then
				local tweenTitle = TweenService:Create(Title_7, tweenInfo, {TextTransparency = 0})
				tweenTitle:Play()
				local tweenValue = TweenService:Create(Value, tweenInfo, {TextTransparency = 0})
				tweenValue:Play()
				local tweenDraggable = TweenService:Create(Draggable, tweenInfo, {BackgroundTransparency = 0})
				tweenDraggable:Play()
			else
				local tweenTitle = TweenService:Create(Title_7, tweenInfo, {TextTransparency = 0.6})
				tweenTitle:Play()
				local tweenValue = TweenService:Create(Value, tweenInfo, {TextTransparency = 0.6})
				tweenValue:Play()
				local tweenDraggable = TweenService:Create(Draggable, tweenInfo, {BackgroundTransparency = 0.6})
				tweenDraggable:Play()
			end
		end

		local function UpdateSliderPosition()
			local percentage = math.clamp((currentValue - min) / (max - min), 0, 1)
			Value.Text = string.format("%.1f", currentValue)
			Draggable.Size = UDim2.new(percentage, 0, 1, 0)
			callback(currentValue)
			UpdateTransparency()
		end

		local function StartDragging(input)
			isDragging = true
			if input.UserInputType == Enum.UserInputType.Touch then
				touchID = input.UserInputIndex
			end
			UpdateTransparency()
		end

		local function UpdateDragging(input)
			local inputPosition
			if input.UserInputType == Enum.UserInputType.MouseMovement then
				inputPosition = input.Position.X
			elseif input.UserInputType == Enum.UserInputType.Touch then
				inputPosition = input.Position.X
			end

			if isDragging then
				local sliderX = SliderBack.AbsolutePosition.X
				local sliderWidth = SliderBack.AbsoluteSize.X
				local newPercentage = math.clamp((inputPosition - sliderX) / sliderWidth, 0, 1)
				currentValue = min + (newPercentage * (max - min))
				currentValue = math.round(currentValue * 10) / 10
				UpdateSliderPosition()
			end
		end

		local function StopDragging(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				isDragging = false
				touchID = nil
				UpdateTransparency()
			end
		end

		Slider.MouseButton1Down:Connect(StartDragging)
		UIS.InputChanged:Connect(UpdateDragging)
		UIS.InputEnded:Connect(StopDragging)

		UpdateSliderPosition()
	end
	
	function lib:CreateInput(title, TabParent, callback)
		local Textbox = Instance.new("ImageButton")
		local UICorner_16 = Instance.new("UICorner")
		local Title_8 = Instance.new("TextLabel")
		local Input = Instance.new("TextBox")
		local UICorner_17 = Instance.new("UICorner")

		Textbox.Name = "Textbox"
		Textbox.Parent = TabParent
		Textbox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Textbox.BackgroundTransparency = 0.500
		Textbox.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Textbox.BorderSizePixel = 0
		Textbox.Position = UDim2.new(0.0271317828, 0, 0.120915033, 0)
		Textbox.Size = UDim2.new(0, 366, 0, 37)
		Textbox.AutoButtonColor = false

		UICorner_16.Parent = Textbox

		Title_8.Name = "Title"
		Title_8.Parent = Textbox
		Title_8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.BackgroundTransparency = 1.000
		Title_8.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_8.BorderSizePixel = 0
		Title_8.Position = UDim2.new(0.0292261671, 0, 0.108107693, 0)
		Title_8.Size = UDim2.new(0, 134, 0, 28)
		Title_8.Font = Enum.Font.SourceSans
		Title_8.Text = title
		Title_8.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.TextSize = 18.000
		Title_8.TextTransparency = 0.600
		Title_8.TextXAlignment = Enum.TextXAlignment.Left

		Input.Name = "Input"
		Input.Parent = Textbox
		Input.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Input.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Input.BorderSizePixel = 0
		Input.Position = UDim2.new(0.841530025, 0, 0.189189196, 0)
		Input.Size = UDim2.new(0, 47, 0, 22)
		Input.Font = Enum.Font.SourceSans
		Input.Text = "Input"
		Input.TextColor3 = Color3.fromRGB(255, 255, 255)
		Input.TextSize = 14.000
		Input.TextTransparency = 0.600

		UICorner_17.CornerRadius = UDim.new(0, 6)
		UICorner_17.Parent = Input

		Input.FocusLost:Connect(function(enteredText)
			if callback then
				callback(enteredText)
			end
		end)
	end

	return lib
end
```
## Create Window
```lua
lib:CreateWindow("Saturn")
```
## Create Tab
```lua
local MagnetTab, MagnetTab = lib:CreateTab("Magnets")
```
## Create Section
```lua
lib:CreateSection("Magnets", MagnetTab)
```
## Create Button
```lua
lib:CreateButton("Who made the ui?", MagnetTab, function()
	print("JUSTVPN")
end)
```
## Create Toggle
```lua
lib:CreateToggle("Show Hitbox", MagnetTab, function(state)
	print("Magnet toggle state:", state)
end)
```
## Create Slider
```lua
lib:CreateSlider("Brute Tween Delay", MagnetTab, 0, 1, function(value)
	print("Current Value: " .. value)
end)
```
## Create Input
```lua
lib:CreateInput("Enter your name", MagnetTab, function(inputText)
	print("User entered:", inputText)
end)
```
