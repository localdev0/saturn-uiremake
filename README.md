## Get Stuff
```lua
local lib = {}
local ThemeUI = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(3, 6, 30)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(8, 26, 91))}

function lib:NewWindow(title)
	local UI = Instance.new("ScreenGui")
	local Main = Instance.new("Frame")
	local UIGradient = Instance.new("UIGradient")
	local UICorner = Instance.new("UICorner")
	local TopBar = Instance.new("Frame")
	local Line = Instance.new("Frame")
	local Title = Instance.new("TextLabel")
	local Navigation = Instance.new("ScrollingFrame")
	local UIListLayout = Instance.new("UIListLayout")
	local UIPadding = Instance.new("UIPadding")
	local Line_2 = Instance.new("Frame")
	local Content = Instance.new("Frame")
	local ToolHolder = Instance.new("Frame")
	local UIPadding_3 = Instance.new("UIPadding")
	local UIListLayout_3 = Instance.new("UIListLayout")
	
	UI.Name = "UI"
	UI.Parent = game:GetService("Players").LocalPlayer.PlayerGui or game:GetService("CoreGui")
	UI.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	UI.DisplayOrder = 999999999
	UI.ResetOnSpawn = false

	Main.Name = "Main"
	Main.Parent = UI
	Main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Main.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Main.BorderSizePixel = 0
	Main.Position = UDim2.new(0, 425, 0, 150)
	Main.Size = UDim2.new(0, 622, 0, 369)

	UIGradient.Color = ThemeUI
	UIGradient.Parent = Main

	UICorner.CornerRadius = UDim.new(0, 10)
	UICorner.Parent = Main

	TopBar.Name = "TopBar"
	TopBar.Parent = Main
	TopBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	TopBar.BackgroundTransparency = 1.000
	TopBar.BorderColor3 = Color3.fromRGB(0, 0, 0)
	TopBar.BorderSizePixel = 0
	TopBar.Size = UDim2.new(0, 573, 0, 49)

	Line.Name = "Line"
	Line.Parent = Main
	Line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Line.BackgroundTransparency = 0.700
	Line.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line.BorderSizePixel = 0
	Line.Position = UDim2.new(0, 0, 0.133081704, 0)
	Line.Size = UDim2.new(0, 622, 0, 1)

	Title.Name = "Title"
	Title.Parent = Main
	Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Title.BackgroundTransparency = 1.000
	Title.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Title.BorderSizePixel = 0
	Title.Position = UDim2.new(0.0349040143, 0, 0, 0)
	Title.Size = UDim2.new(0, 180, 0, 50)
	Title.Font = Enum.Font.GothamBold
	Title.Text = title
	Title.TextColor3 = Color3.fromRGB(255, 255, 255)
	Title.TextSize = 28.000
	Title.TextTransparency = 0.300
	Title.TextXAlignment = Enum.TextXAlignment.Left

	Navigation.Name = "Navigation"
	Navigation.Parent = Main
	Navigation.Active = true
	Navigation.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Navigation.BackgroundTransparency = 1.000
	Navigation.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.BorderSizePixel = 0
	Navigation.Position = UDim2.new(0, 0, 0.132791325, 0)
	Navigation.Size = UDim2.new(0, 134, 0, 320)
	Navigation.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
	Navigation.CanvasSize = UDim2.new(0, 0, 7, 0)
	Navigation.ScrollBarThickness = 0

	UIListLayout.Parent = Navigation
	UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout.Padding = UDim.new(0, 4)

	UIPadding.Parent = Navigation
	UIPadding.PaddingTop = UDim.new(0, 4)
	
	Line_2.Name = "Line"
	Line_2.Parent = Main
	Line_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Line_2.BackgroundTransparency = 0.700
	Line_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Line_2.BorderSizePixel = 0
	Line_2.Position = UDim2.new(0.217014626, 0, 0.135501355, 0)
	Line_2.Size = UDim2.new(0, 1, 0, 319)

	Content.Name = "Content"
	Content.Parent = Main
	Content.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	Content.BackgroundTransparency = 1.000
	Content.BorderColor3 = Color3.fromRGB(0, 0, 0)
	Content.BorderSizePixel = 0
	Content.Position = UDim2.new(0.217041805, 0, 0.135501355, 0)
	Content.Size = UDim2.new(0, 487, 0, 319)
	
	ToolHolder.Name = "ToolHolder"
	ToolHolder.Parent = UI
	ToolHolder.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ToolHolder.BorderColor3 = Color3.fromRGB(0, 0, 0)
	ToolHolder.BorderSizePixel = 0
	ToolHolder.Position = UDim2.new(0.747959197, 0, 0.245000005, 0)
	ToolHolder.Size = UDim2.new(0, 240, 0, 0)

	UIPadding_3.Parent = ToolHolder
	UIPadding_3.PaddingTop = UDim.new(0, 4)

	UIListLayout_3.Parent = ToolHolder
	UIListLayout_3.HorizontalAlignment = Enum.HorizontalAlignment.Center
	UIListLayout_3.SortOrder = Enum.SortOrder.LayoutOrder
	UIListLayout_3.Padding = UDim.new(0, 3)
	
	local function RUUUW_script()
		local script = Instance.new('LocalScript', Main)

		local TweenService = game:GetService("TweenService")
		local UserInputService = game:GetService("UserInputService")

		local gui = script.Parent

		local dragging
		local dragInput
		local dragStart
		local startPos

		local tweenInfo = TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)

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

		local function toggleGuiVisibility(input)
			if input.UserInputType == Enum.UserInputType.Keyboard and input.KeyCode == Enum.KeyCode.LeftControl then
				gui.Visible = not gui.Visible
			end
		end

		UserInputService.InputBegan:Connect(function(input, gameProcessed)
			if not gameProcessed then
				toggleGuiVisibility(input)
			end
		end)

	end
	coroutine.wrap(RUUUW_script)()
	
	local TweenService = game:GetService("TweenService")

	function lib:NewTab(title)
		local Tab = Instance.new("TextButton")
		local UICorner_3 = Instance.new("UICorner")
		local ActiveLine_2 = Instance.new("Frame")
		local Items = Instance.new("ScrollingFrame")
		local UIPadding_2 = Instance.new("UIPadding")
		local UIListLayout_2 = Instance.new("UIListLayout")

		Tab.Name = "Tab"
		Tab.Parent = Navigation
		Tab.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Tab.BackgroundTransparency = 1.000
		Tab.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Tab.BorderSizePixel = 0
		Tab.Position = UDim2.new(0.0688155591, 0, 0, 0)
		Tab.Size = UDim2.new(0, 115, 0, 35)
		Tab.AutoButtonColor = false
		Tab.Font = Enum.Font.Gotham
		Tab.Text = title
		Tab.TextColor3 = Color3.fromRGB(255, 255, 255)
		Tab.TextSize = 16.000
		Tab.TextTransparency = 0.400

		UICorner_3.CornerRadius = UDim.new(0, 6)
		UICorner_3.Parent = Tab

		ActiveLine_2.Name = "ActiveLine"
		ActiveLine_2.Parent = Tab
		ActiveLine_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		ActiveLine_2.BackgroundTransparency = 1.000
		ActiveLine_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ActiveLine_2.BorderSizePixel = 0
		ActiveLine_2.Position = UDim2.new(0.0489804894, 0, 0.171428576, 0)
		ActiveLine_2.Size = UDim2.new(0, 2, 0, 22)

		Items.Name = title
		Items.Parent = Content
		Items.Active = true
		Items.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Items.BackgroundTransparency = 1.000
		Items.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Items.BorderSizePixel = 0
		Items.Size = UDim2.new(0, 0, 0, 319)  -- Initial size set to (0, 0)
		Items.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)
		Items.CanvasSize = UDim2.new(0, 0, 15, 0)
		Items.ScrollBarThickness = 0
		Items.Visible = false  -- Start with visibility off

		UIPadding_2.Parent = Items
		UIPadding_2.PaddingTop = UDim.new(0, 4)

		UIListLayout_2.Parent = Items
		UIListLayout_2.HorizontalAlignment = Enum.HorizontalAlignment.Center
		UIListLayout_2.SortOrder = Enum.SortOrder.LayoutOrder
		UIListLayout_2.Padding = UDim.new(0, 3)

		Tab.MouseButton1Click:Connect(function()
			for _, otherTab in pairs(Navigation:GetChildren()) do
				if otherTab:IsA("TextButton") then
					local otherLine = otherTab:FindFirstChild("ActiveLine")
					local otherItems = Content:FindFirstChild(otherTab.Text)

					if otherTab == Tab then
						TweenService:Create(Tab, TweenInfo.new(0.3), {BackgroundTransparency = 0.5}):Play()
						TweenService:Create(ActiveLine_2, TweenInfo.new(0.3), {BackgroundTransparency = 0}):Play()

						Items.Visible = true
						local fadeInTween = TweenService:Create(Items, TweenInfo.new(0.6), {BackgroundTransparency = 1, Size = UDim2.new(0, 487, 0, 319)})
						fadeInTween:Play()

					else
						TweenService:Create(otherTab, TweenInfo.new(0.3), {BackgroundTransparency = 1}):Play()
						TweenService:Create(otherLine, TweenInfo.new(0.3), {BackgroundTransparency = 1}):Play()

						local fadeOutTween = TweenService:Create(otherItems, TweenInfo.new(0.6), {BackgroundTransparency = 1, Size = UDim2.new(0, 0, 0, 319)})
						fadeOutTween:Play()
						otherItems.Visible = false
					end
				end
			end
		end)

		return Items
	end

	
	function lib:NewSection(title, TabParent)
		local Section = Instance.new("Frame")
		local UICorner_4 = Instance.new("UICorner")
		
		Section.Name = title
		Section.Parent = TabParent
		Section.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Section.BackgroundTransparency = 0.500
		Section.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Section.BorderSizePixel = 0
		Section.Position = UDim2.new(0.397330582, 0, 0.650793672, 0)
		Section.Size = UDim2.new(0, 399, 0, 3)

		UICorner_4.CornerRadius = UDim.new(1, 0)
		UICorner_4.Parent = Section
	end
	
	local TweenService = game:GetService("TweenService")

	function lib:NewButton(title, TabParent, toolTipText, callback)
		local Button = Instance.new("ImageButton")
		local UICorner_20 = Instance.new("UICorner")
		local Title_8 = Instance.new("TextLabel")
		local MouseIcon = Instance.new("ImageLabel")
		local UIAspectRatioConstraint_3 = Instance.new("UIAspectRatioConstraint")
		local ToolTip = Instance.new("Frame")
		local UICorner_21 = Instance.new("UICorner")
		local ToolTitle = Instance.new("TextLabel")
		local UIStroke_2 = Instance.new("UIStroke")

		Button.Name = "Button"
		Button.Parent = TabParent
		Button.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Button.BackgroundTransparency = 0.500
		Button.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Button.BorderSizePixel = 0
		Button.Position = UDim2.new(-0.0585215613, 0, 0.387301594, 0)
		Button.Size = UDim2.new(0, 472, 0, 38)
		Button.AutoButtonColor = false

		UICorner_20.CornerRadius = UDim.new(0, 6)
		UICorner_20.Parent = Button

		Title_8.Name = "Title"
		Title_8.Parent = Button
		Title_8.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.BackgroundTransparency = 1.000
		Title_8.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_8.BorderSizePixel = 0
		Title_8.Position = UDim2.new(0.0254237279, 0, -0.0234961268, 0)
		Title_8.Size = UDim2.new(0, 234, 0, 38)
		Title_8.Font = Enum.Font.Gotham
		Title_8.Text = title
		Title_8.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_8.TextSize = 15.000
		Title_8.TextXAlignment = Enum.TextXAlignment.Left

		MouseIcon.Name = "MouseIcon"
		MouseIcon.Parent = Button
		MouseIcon.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		MouseIcon.BackgroundTransparency = 1.000
		MouseIcon.BorderColor3 = Color3.fromRGB(0, 0, 0)
		MouseIcon.BorderSizePixel = 0
		MouseIcon.Position = UDim2.new(0.924355984, 0, 0.184210524, 0)
		MouseIcon.Size = UDim2.new(0, 24, 0, 34)
		MouseIcon.Image = "rbxassetid://12804017021"

		UIAspectRatioConstraint_3.Parent = MouseIcon

		ToolTip.Name = "ToolTip"
		ToolTip.Parent = TabParent
		ToolTip.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderSizePixel = 0
		ToolTip.BackgroundTransparency = 0.3
		ToolTip.Position = UDim2.new(0.00833333377, 0, -0.0893554688, 0)
		ToolTip.Size = UDim2.new(0, 420, 0, 34)
		ToolTip.Visible = false

		UICorner_21.CornerRadius = UDim.new(0, 4)
		UICorner_21.Parent = ToolTip

		ToolTitle.Name = "ToolTitle"
		ToolTitle.Parent = ToolTip
		ToolTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.BackgroundTransparency = 1.000
		ToolTitle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTitle.BorderSizePixel = 0
		ToolTitle.Position = UDim2.new(0.0423728824, 0, -0.028801702, 0)
		ToolTitle.Size = UDim2.new(0, 226, 0, 34)
		ToolTitle.Font = Enum.Font.SourceSans
		ToolTitle.Text = toolTipText
		ToolTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.TextSize = 18.000
		ToolTitle.TextXAlignment = Enum.TextXAlignment.Left

		local tooltipTweenInfo = TweenInfo.new(0.25, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
		local tooltipVisibleTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 34), Transparency = 0.5})
		local tooltipHiddenTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 0), Transparency = 1})

		Button.MouseEnter:Connect(function()
			ToolTip.Visible = true
			tooltipVisibleTween:Play()
		end)

		Button.MouseLeave:Connect(function()
			tooltipHiddenTween:Play()
			tooltipHiddenTween.Completed:Connect(function()
				ToolTip.Visible = false
			end)
		end)

		Button.MouseButton1Click:Connect(function()
			if callback then
				callback()
			end
		end)

		return Button
	end

	local TweenService = game:GetService("TweenService")
	local UserInputService = game:GetService("UserInputService")
	
	function lib:NewToggle(title, tabParent, toolTipText, callback)
	    local Toggle = Instance.new("ImageButton")
	    local UICorner_8 = Instance.new("UICorner")
	    local Title_3 = Instance.new("TextLabel")
	    local Checkbox_2 = Instance.new("Frame")
	    local UIAspectRatioConstraint_2 = Instance.new("UIAspectRatioConstraint")
	    local UICorner_9 = Instance.new("UICorner")
	    local Checkmark_2 = Instance.new("ImageLabel")
	    local UICorner_10 = Instance.new("UICorner")
	    local KeybindToggleBox_2 = Instance.new("TextBox")
	    local ToolTip = Instance.new("Frame")
	    local UICorner_21 = Instance.new("UICorner")
	    local ToolTitle = Instance.new("TextLabel")
	    local UIStroke_2 = Instance.new("UIStroke")
	
	    Toggle.Name = "Toggle"
	    Toggle.Parent = tabParent
	    Toggle.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	    Toggle.BackgroundTransparency = 0.5
	    Toggle.BorderSizePixel = 0
	    Toggle.Size = UDim2.new(0, 472, 0, 38)
	    Toggle.AutoButtonColor = false
	    UICorner_8.CornerRadius = UDim.new(0, 6)
	    UICorner_8.Parent = Toggle
	
	    Title_3.Name = "Title"
	    Title_3.Parent = Toggle
	    Title_3.BackgroundTransparency = 1
	    Title_3.Position = UDim2.new(0.025, 0, 0, 0)
	    Title_3.Size = UDim2.new(0, 234, 0, 38)
	    Title_3.Font = Enum.Font.Gotham
	    Title_3.Text = title
	    Title_3.TextColor3 = Color3.fromRGB(255, 255, 255)
	    Title_3.TextSize = 15
	    Title_3.TextXAlignment = Enum.TextXAlignment.Left
	
	    Checkbox_2.Name = "Checkbox"
	    Checkbox_2.Parent = Toggle
	    Checkbox_2.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
	    Checkbox_2.Position = UDim2.new(0.918, 0, 0.122, 0)
	    Checkbox_2.Size = UDim2.new(0, 32, 0, 29)
	    UICorner_9.CornerRadius = UDim.new(0, 4)
	    UICorner_9.Parent = Checkbox_2
	    UIAspectRatioConstraint_2.Parent = Checkbox_2
	    UIAspectRatioConstraint_2.AspectRatio = 1.13
	
	    Checkmark_2.Name = "Checkmark"
	    Checkmark_2.Parent = Checkbox_2
	    Checkmark_2.BackgroundTransparency = 1
	    Checkmark_2.Size = UDim2.new(0, 25, 0, 22)
	    Checkmark_2.Image = "rbxassetid://10709790644"
	    Checkmark_2.ImageTransparency = 1
	    Checkmark_2.Position = UDim2.new(0.09375, 0, 0.118791193, 0)
	
	    KeybindToggleBox_2.Name = "KeybindToggleBox"
	    KeybindToggleBox_2.Parent = Toggle
	    KeybindToggleBox_2.BackgroundTransparency = 1
	    KeybindToggleBox_2.Position = UDim2.new(0.739, 0, 0, 0)
	    KeybindToggleBox_2.Size = UDim2.new(0, 78, 0, 38)
	    KeybindToggleBox_2.Font = Enum.Font.SourceSans
	    KeybindToggleBox_2.PlaceholderText = "Click To Bind"
	    KeybindToggleBox_2.Text = ""
	    KeybindToggleBox_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	    KeybindToggleBox_2.TextSize = 17
	    KeybindToggleBox_2.TextXAlignment = Enum.TextXAlignment.Left
	
	    ToolTip.Name = "Tooltip"
	    ToolTip.Parent = tabParent
	    ToolTip.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	    ToolTip.BackgroundTransparency = 0.3
	    ToolTip.Position = UDim2.new(0.008, 0, -0.089, 0)
	    ToolTip.Size = UDim2.new(0, 420, 0, 34)
	    ToolTip.Visible = false
	    UICorner_21.CornerRadius = UDim.new(0, 4)
	    UICorner_21.Parent = ToolTip
	
	    ToolTitle.Name = "ToolTitle"
	    ToolTitle.Parent = ToolTip
	    ToolTitle.BackgroundTransparency = 1
	    ToolTitle.Position = UDim2.new(0.042, 0, 0, 0)
	    ToolTitle.Size = UDim2.new(0, 226, 0, 34)
	    ToolTitle.Font = Enum.Font.SourceSans
	    ToolTitle.Text = toolTipText
	    ToolTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
	    ToolTitle.TextSize = 18
	
	    local tooltipTweenInfo = TweenInfo.new(0.25, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
		local tooltipVisibleTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 34), Transparency = 0.5})
		local tooltipHiddenTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 0), Transparency = 1})
	
	    Toggle.MouseEnter:Connect(function()
			ToolTip.Visible = true
			tooltipVisibleTween:Play()
		end)

		Toggle.MouseLeave:Connect(function()
			tooltipHiddenTween:Play()
			tooltipHiddenTween.Completed:Connect(function()
				ToolTip.Visible = false
			end)
		end)
	
	    local toggleState = false
	    local boundKey
	
	    local function updateToggle(state)
	        local targetTransparency = state and 0 or 1
	        TweenService:Create(Checkmark_2, TweenInfo.new(0.2), {ImageTransparency = targetTransparency}):Play()
	        if callback then
	            callback(state)
	        end
	    end
	
	    Toggle.MouseButton1Click:Connect(function()
	        toggleState = not toggleState
	        updateToggle(toggleState)
	    end)
	
	    KeybindToggleBox_2.FocusLost:Connect(function(enterPressed)
	        if enterPressed then
	            local inputText = KeybindToggleBox_2.Text:upper()
	            if #inputText == 1 and inputText:match("%a") then
	                boundKey = inputText
	                KeybindToggleBox_2.Text = "Bind: " .. boundKey
	            else
	                KeybindToggleBox_2.Text = ""
	            end
	        end
	    end)
	
	    UserInputService.InputBegan:Connect(function(input, isProcessed)
	        if not isProcessed and input.KeyCode.Name == boundKey then
	            toggleState = not toggleState
	            updateToggle(toggleState)
	        end
	    end)
	end
	
	local UserInputService = game:GetService("UserInputService")

	function lib:NewSlider(title, TabParent, min, max, default, toolTipText, callback)
		local Slider = Instance.new("ImageButton")
		local UICorner_11 = Instance.new("UICorner")
		local Title_4 = Instance.new("TextLabel")
		local SliderBack = Instance.new("Frame")
		local UICorner_12 = Instance.new("UICorner")
		local Draggable = Instance.new("Frame")
		local UICorner_13 = Instance.new("UICorner")
		local Value = Instance.new("TextLabel")
		local ToolTip = Instance.new("Frame")
		local UICorner_21 = Instance.new("UICorner")
		local ToolTitle = Instance.new("TextLabel")
		local UIStroke_2 = Instance.new("UIStroke")

		Slider.Name = "Slider"
		Slider.Parent = TabParent
		Slider.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BackgroundTransparency = 0.500
		Slider.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Slider.BorderSizePixel = 0
		Slider.Position = UDim2.new(0.0154004106, 0, 0, 0)
		Slider.Size = UDim2.new(0, 472, 0, 38)
		Slider.AutoButtonColor = false

		UICorner_11.CornerRadius = UDim.new(0, 6)
		UICorner_11.Parent = Slider

		Title_4.Name = "Title"
		Title_4.Parent = Slider
		Title_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.BackgroundTransparency = 1.000
		Title_4.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_4.BorderSizePixel = 0
		Title_4.Position = UDim2.new(0.0254237279, 0, -0.0234961268, 0)
		Title_4.Size = UDim2.new(0, 234, 0, 38)
		Title_4.Font = Enum.Font.Gotham
		Title_4.Text = title
		Title_4.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_4.TextSize = 15.000
		Title_4.TextXAlignment = Enum.TextXAlignment.Left

		SliderBack.Name = "SliderBack"
		SliderBack.Parent = Slider
		SliderBack.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
		SliderBack.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SliderBack.BorderSizePixel = 0
		SliderBack.Position = UDim2.new(0.506983101, 0, 0.411473721, 0)
		SliderBack.Size = UDim2.new(0, 226, 0, 6)

		UICorner_12.CornerRadius = UDim.new(0, 4)
		UICorner_12.Parent = SliderBack

		Draggable.Name = "Draggable"
		Draggable.Parent = SliderBack
		Draggable.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Draggable.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Draggable.BorderSizePixel = 0
		Draggable.Position = UDim2.new(-0.00186643342, 0, -0.0885264054, 0)
		Draggable.Size = UDim2.new(0, 162, 0, 6)

		UICorner_13.CornerRadius = UDim.new(0, 4)
		UICorner_13.Parent = Draggable

		Value.Name = "Value"
		Value.Parent = Slider
		Value.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Value.BackgroundTransparency = 1.000
		Value.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Value.BorderSizePixel = 0
		Value.Position = UDim2.new(0.387711853, 0, -0.0234961268, 0)
		Value.Size = UDim2.new(0, 49, 0, 38)
		Value.Font = Enum.Font.Gotham
		Value.Text = tostring(default)
		Value.TextColor3 = Color3.fromRGB(255, 255, 255)
		Value.TextSize = 15.000
		Value.TextXAlignment = Enum.TextXAlignment.Right
		
		ToolTip.Name = "Tooptip"
		ToolTip.Parent = TabParent
		ToolTip.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderSizePixel = 0
		ToolTip.BackgroundTransparency = 0.3
		ToolTip.Position = UDim2.new(0.00833333377, 0, -0.0893554688, 0)
		ToolTip.Size = UDim2.new(0, 420, 0, 34)
		ToolTip.Visible = false

		UICorner_21.CornerRadius = UDim.new(0, 4)
		UICorner_21.Parent = ToolTip

		ToolTitle.Name = "ToolTitle"
		ToolTitle.Parent = ToolTip
		ToolTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.BackgroundTransparency = 1.000
		ToolTitle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTitle.BorderSizePixel = 0
		ToolTitle.Position = UDim2.new(0.0423728824, 0, -0.028801702, 0)
		ToolTitle.Size = UDim2.new(0, 226, 0, 34)
		ToolTitle.Font = Enum.Font.SourceSans
		ToolTitle.Text = toolTipText
		ToolTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.TextSize = 18.000
		ToolTitle.TextXAlignment = Enum.TextXAlignment.Left

		local tooltipTweenInfo = TweenInfo.new(0.25, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
		local tooltipVisibleTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 34), Transparency = 0.5})
		local tooltipHiddenTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 0), Transparency = 1})

		Slider.MouseEnter:Connect(function()
			ToolTip.Visible = true
			tooltipVisibleTween:Play()
		end)

		Slider.MouseLeave:Connect(function()
			tooltipHiddenTween:Play()
			tooltipHiddenTween.Completed:Connect(function()
				ToolTip.Visible = false
			end)
		end)

		Slider.MouseButton1Click:Connect(function()
			if callback then
				callback()
			end
		end)

		local currentValue = min
		local isDragging = false
		local touchID = nil

		local function UpdateSliderPosition()
			local percentage = math.clamp((currentValue - min) / (max - min), 0, 1)
			Value.Text = string.format("%.1f", currentValue)
			Draggable.Size = UDim2.new(percentage, 0, 1, 0)
			callback(currentValue)
		end

		local function StartDragging(input)
			isDragging = true
			if input.UserInputType == Enum.UserInputType.Touch then
				touchID = input.UserInputIndex
			end
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
			end
		end

		Slider.MouseButton1Down:Connect(StartDragging)
		UserInputService.InputChanged:Connect(UpdateDragging)
		UserInputService.InputEnded:Connect(StopDragging)

		currentValue = default
		UpdateSliderPosition()
	end
	
	function lib:NewDropdown(title, TabParent, options, toolTipText, callback)
		local Dropdown = Instance.new("ImageButton")
		local UICorner_14 = Instance.new("UICorner")
		local Title_5 = Instance.new("TextLabel")
		local Checkbox_3 = Instance.new("Frame")
		local UICorner_15 = Instance.new("UICorner")
		local SelectedText = Instance.new("TextLabel")
		local ToolTip = Instance.new("Frame")
		local UICorner_21 = Instance.new("UICorner")
		local ToolTitle = Instance.new("TextLabel")
		local UIStroke_2 = Instance.new("UIStroke")

		Dropdown.Name = "Dropdown"
		Dropdown.Parent = TabParent
		Dropdown.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Dropdown.BackgroundTransparency = 0.500
		Dropdown.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Dropdown.BorderSizePixel = 0
		Dropdown.Position = UDim2.new(0, 0, 0.387301594, 0)
		Dropdown.Size = UDim2.new(0, 472, 0, 38)
		Dropdown.AutoButtonColor = false

		UICorner_14.CornerRadius = UDim.new(0, 6)
		UICorner_14.Parent = Dropdown

		Title_5.Name = "Title"
		Title_5.Parent = Dropdown
		Title_5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.BackgroundTransparency = 1.000
		Title_5.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_5.BorderSizePixel = 0
		Title_5.Position = UDim2.new(0.0254237279, 0, -0.0234961268, 0)
		Title_5.Size = UDim2.new(0, 234, 0, 38)
		Title_5.Font = Enum.Font.Gotham
		Title_5.Text = title
		Title_5.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_5.TextSize = 15.000
		Title_5.TextXAlignment = Enum.TextXAlignment.Left

		Checkbox_3.Name = "Checkbox"
		Checkbox_3.Parent = Dropdown
		Checkbox_3.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
		Checkbox_3.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Checkbox_3.BorderSizePixel = 0
		Checkbox_3.Position = UDim2.new(0.668000042, 0, 0.121999644, 0)
		Checkbox_3.Size = UDim2.new(0, 150, 0, 29)

		UICorner_15.CornerRadius = UDim.new(0, 4)
		UICorner_15.Parent = Checkbox_3

		SelectedText.Name = "SelectedText"
		SelectedText.Parent = Checkbox_3
		SelectedText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.BackgroundTransparency = 1.000
		SelectedText.BorderColor3 = Color3.fromRGB(0, 0, 0)
		SelectedText.BorderSizePixel = 0
		SelectedText.Size = UDim2.new(0, 150, 0, 29)
		SelectedText.Font = Enum.Font.Gotham
		SelectedText.Text = "Select an option"
		SelectedText.TextColor3 = Color3.fromRGB(255, 255, 255)
		SelectedText.TextSize = 15.000

		local DropHolder = Instance.new("Frame")
		local UIPadding_4 = Instance.new("UIPadding")
		local UIListLayout_4 = Instance.new("UIListLayout")

		DropHolder.Name = "DropHolder"
		DropHolder.Parent = UI
		DropHolder.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		DropHolder.BorderColor3 = Color3.fromRGB(0, 0, 0)
		DropHolder.BorderSizePixel = 0
		DropHolder.Position = UDim2.new(0.75, 0, 0.322878242, 0)
		DropHolder.Size = UDim2.new(0, 236, 0, 0)
		DropHolder.Visible = false

		UIPadding_4.Parent = DropHolder
		UIPadding_4.PaddingTop = UDim.new(0, 4)

		UIListLayout_4.Parent = DropHolder
		UIListLayout_4.HorizontalAlignment = Enum.HorizontalAlignment.Center
		UIListLayout_4.SortOrder = Enum.SortOrder.LayoutOrder
		UIListLayout_4.Padding = UDim.new(0, 0)
		
		ToolTip.Name = "Tooptip"
		ToolTip.Parent = TabParent
		ToolTip.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTip.BorderSizePixel = 0
		ToolTip.BackgroundTransparency = 0.3
		ToolTip.Position = UDim2.new(0.00833333377, 0, -0.0893554688, 0)
		ToolTip.Size = UDim2.new(0, 420, 0, 34)
		ToolTip.Visible = false

		UICorner_21.CornerRadius = UDim.new(0, 4)
		UICorner_21.Parent = ToolTip

		ToolTitle.Name = "ToolTitle"
		ToolTitle.Parent = ToolTip
		ToolTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.BackgroundTransparency = 1.000
		ToolTitle.BorderColor3 = Color3.fromRGB(0, 0, 0)
		ToolTitle.BorderSizePixel = 0
		ToolTitle.Position = UDim2.new(0.0423728824, 0, -0.028801702, 0)
		ToolTitle.Size = UDim2.new(0, 226, 0, 34)
		ToolTitle.Font = Enum.Font.SourceSans
		ToolTitle.Text = toolTipText
		ToolTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
		ToolTitle.TextSize = 18.000
		ToolTitle.TextXAlignment = Enum.TextXAlignment.Left

		local tooltipTweenInfo = TweenInfo.new(0.25, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
		local tooltipVisibleTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 34), Transparency = 0.5})
		local tooltipHiddenTween = TweenService:Create(ToolTip, tooltipTweenInfo, {Size = UDim2.new(0, 420, 0, 0), Transparency = 1})

		Dropdown.MouseEnter:Connect(function()
			ToolTip.Visible = true
			tooltipVisibleTween:Play()
		end)

		Dropdown.MouseLeave:Connect(function()
			tooltipHiddenTween:Play()
			tooltipHiddenTween.Completed:Connect(function()
				ToolTip.Visible = false
			end)
		end)

		Dropdown.MouseButton1Click:Connect(function()
			if callback then
				callback()
			end
		end)

		Dropdown.MouseButton1Click:Connect(function()
			DropHolder.Visible = not DropHolder.Visible
		end)

		for i, option in ipairs(options) do
			local DropButton = Instance.new("TextButton")
			local ActiveLine_3 = Instance.new("Frame")

			DropButton.Name = "DropButton"
			DropButton.Parent = DropHolder
			DropButton.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
			DropButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
			DropButton.BorderSizePixel = 0
			DropButton.Position = UDim2.new(0.319915265, 0, (i - 1) * 0.35, 0)
			DropButton.Size = UDim2.new(0, 115, 0, 35)
			DropButton.AutoButtonColor = false
			DropButton.Font = Enum.Font.SourceSans
			DropButton.Text = option
			DropButton.TextColor3 = Color3.fromRGB(255, 255, 255)
			DropButton.TextSize = 19.000

			ActiveLine_3.Name = "ActiveLine"
			ActiveLine_3.Parent = DropButton
			ActiveLine_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			ActiveLine_3.BorderColor3 = Color3.fromRGB(0, 0, 0)
			ActiveLine_3.BorderSizePixel = 0
			ActiveLine_3.Position = UDim2.new(0.0173913036, 0, -0.0104003903, 0)
			ActiveLine_3.Size = UDim2.new(0, -2, 0, 35)

			DropButton.MouseButton1Click:Connect(function()
				SelectedText.Text = option
				callback(option)
				DropHolder.Visible = false
			end)
		end
	end

	function lib:NewInput(title, TabParent, toolTipText, callback)
		local Input = Instance.new("ImageButton")
		local UICorner_16 = Instance.new("UICorner")
		local Title_6 = Instance.new("TextLabel")
		local Checkbox_4 = Instance.new("Frame")
		local UICorner_17 = Instance.new("UICorner")
		local TextBox = Instance.new("TextBox")

		Input.Name = "Input"
		Input.Parent = TabParent
		Input.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Input.BackgroundTransparency = 0.500
		Input.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Input.BorderSizePixel = 0
		Input.Position = UDim2.new(0.0462012328, 0, 0.51111114, 0)
		Input.Size = UDim2.new(0, 472, 0, 38)
		Input.AutoButtonColor = false

		UICorner_16.CornerRadius = UDim.new(0, 6)
		UICorner_16.Parent = Input

		Title_6.Name = "Title"
		Title_6.Parent = Input
		Title_6.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.BackgroundTransparency = 1.000
		Title_6.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Title_6.BorderSizePixel = 0
		Title_6.Position = UDim2.new(0.0254237279, 0, -0.0234961268, 0)
		Title_6.Size = UDim2.new(0, 234, 0, 38)
		Title_6.Font = Enum.Font.Gotham
		Title_6.Text = title
		Title_6.TextColor3 = Color3.fromRGB(255, 255, 255)
		Title_6.TextSize = 15.000
		Title_6.TextXAlignment = Enum.TextXAlignment.Left

		Checkbox_4.Name = "Checkbox"
		Checkbox_4.Parent = Input
		Checkbox_4.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
		Checkbox_4.BorderColor3 = Color3.fromRGB(0, 0, 0)
		Checkbox_4.BorderSizePixel = 0
		Checkbox_4.Position = UDim2.new(0.788762748, 0, 0.121999644, 0)
		Checkbox_4.Size = UDim2.new(0, 93, 0, 29)

		UICorner_17.CornerRadius = UDim.new(0, 4)
		UICorner_17.Parent = Checkbox_4

		TextBox.Parent = Checkbox_4
		TextBox.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.BackgroundTransparency = 1.000
		TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
		TextBox.BorderSizePixel = 0
		TextBox.Position = UDim2.new(0.0106384931, 0, 0, 0)
		TextBox.Size = UDim2.new(0, 93, 0, 28)
		TextBox.Font = Enum.Font.Gotham
		TextBox.PlaceholderText = "Enter"
		TextBox.Text = ""
		TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
		TextBox.TextSize = 16.000

		TextBox.FocusLost:Connect(function(enterPressed)
			if enterPressed then
				callback(TextBox.Text)
			end
		end)
	end
	
	return lib
end
```
## Create Window
```lua
lib:NewWindow("SHADOW")
```
## Create Tab
```lua
local tab1 = lib:NewTab("Test")
local tab2 = lib:NewTab("ing")
```
## Create Button
```lua
lib:NewButton("Click Me!", tab1, "Copies the discord server to your clipboard", function()
	print("Button clicked!")
end)
```
## Create Toggle
```lua
lib:NewToggle("Example Toggle", tab1, "Example of the toggle", function(state)
	print("Toggle state:", state)
end)
```
## Create Slider
```lua
lib:NewSlider("Volume Control", tab1, 0, 100, 50, "Changes the ball size", function(value)
	print(value)
end)
```
## Create Dropdown
```lua
local options = {"Option 1", "Option 2", "Option 3", "Option 4"}
lib:NewDropdown("Magnet Mode", tab1, options, "Changes the ball size to the mode", function(selectedOption)
	print("You selected: " .. selectedOption)
end)
```
## Create Input
```lua
lib:NewInput("Enter your name:", tab1, function(inputText)
	print("User entered: " .. inputText)
end)
```
