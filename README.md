local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local CoreGui = game:GetService("CoreGui")
local StarterGui = game:GetService("StarterGui")
local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")
local VirtualInputManager = game:GetService("VirtualInputManager")

local lp = Players.LocalPlayer

-- Função que cria a tela de loading e retorna uma promise
local function createLoadingScreen()
    local promise = {}
    promise.completed = false
    promise.connection = nil
    
    pcall(function()
        if CoreGui:FindFirstChild("LoadingScreen") then
            CoreGui.LoadingScreen:Destroy()
        end
    end)

    local gui = Instance.new("ScreenGui")
    gui.Name = "LoadingScreen"
    gui.IgnoreGuiInset = true
    gui.ResetOnSpawn = false
    gui.Parent = CoreGui
    pcall(function() syn.protect_gui(gui) end)

    local frame = Instance.new("Frame")
    frame.BackgroundColor3 = Color3.new(0, 0, 0)
    frame.BackgroundTransparency = 0.3
    frame.Size = UDim2.new(1, 0, 1, 0)
    frame.Parent = gui

    local image = Instance.new("ImageLabel")
    image.Size = UDim2.new(0, 300, 0, 300)
    image.Position = UDim2.new(0.5, -150, 0.35, -150)
    image.BackgroundTransparency = 1
    image.Image = "rbxassetid://75732220851513"
    image.Parent = frame

    local nameText = Instance.new("TextLabel")
    nameText.Size = UDim2.new(1, 0, 0, 40)
    nameText.Position = UDim2.new(0, 0, 0.65, 0)
    nameText.TextColor3 = Color3.fromRGB(255, 255, 255)
    nameText.TextStrokeTransparency = 0.3
    nameText.BackgroundTransparency = 1
    nameText.Font = Enum.Font.FredokaOne
    nameText.TextScaled = true
    nameText.Text = "Verificando usuário: "..lp.Name.." (Conta: "..tostring(lp.AccountAge).." dias)"
    nameText.Parent = frame

    local barBG = Instance.new("Frame")
    barBG.Size = UDim2.new(0.6, 0, 0.03, 0)
    barBG.Position = UDim2.new(0.2, 0, 0.8, 0)
    barBG.BackgroundColor3 = Color3.new(1, 1, 1)
    barBG.BorderSizePixel = 0
    barBG.Parent = frame

    local bar = Instance.new("Frame")
    bar.Size = UDim2.new(0, 0, 1, 0)
    bar.BackgroundColor3 = Color3.new(0.7, 0.2, 0.6)
    bar.BorderSizePixel = 0
    bar.Parent = barBG

    local tween = TweenService:Create(
        bar,
        TweenInfo.new(4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
        {Size = UDim2.new(1, 0, 1, 0)}
    )
    tween:Play()

    local function cleanup()
        if gui then
            gui:Destroy()
        end
        if promise.connection then
            promise.connection:Disconnect()
        end
    end

    promise.connection = tween.Completed:Connect(function()
        TweenService:Create(frame, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(barBG, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(bar, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(image, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {ImageTransparency = 1}):Play()
        TweenService:Create(nameText, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {TextTransparency = 1}):Play()
        
        task.delay(1.2, function()
            local sound = Instance.new("Sound")
            sound.SoundId = "rbxassetid://8486683243"
            sound.Volume = 0.5
            sound.PlayOnRemove = true
            sound.Parent = workspace
            sound:Destroy()
            
            StarterGui:SetCore("SendNotification", {
                Title = "Coquette Hub",
                Text = "Bem-vindo à Coquette Hub 💖",
                Duration = 4
            })
            
            promise.completed = true
            cleanup()
        end)
    end)
    
    return promise
end

local function waitForPromise(promise)
    while not promise.completed do
        task.wait()
    end
end

local loadingPromise = createLoadingScreen()
waitForPromise(loadingPromise)

print("Loading completo! Agora executando o resto do script...")

local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()

local Window = redzlib:MakeWindow({
    Title = "Coquette Hub 3.6",
    SubTitle = "by Lolytadev 💖",
    SaveFolder = "teste"
})

Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://135441295532401", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

local Tab1 = Window:MakeTab({"Blade Ball", "swords"})

-- Variáveis dinâmicas
local LocalPlayer = Players.LocalPlayer
local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
local Ball = nil

-- Função para encontrar a bola dinamicamente
local function FindBall()
    local path = workspace:FindFirstChild("Map") and workspace.Map:FindFirstChild("Grassy_Classic") and workspace.Map.Grassy_Classic:FindFirstChild("Border") and workspace.Map.Grassy_Classic.Border:FindFirstChild("BallFloor")
    if path then
        Ball = path
        print("Bola encontrada:", Ball:GetFullName())
        return true
    else
        print("Bola não encontrada. Tentando novamente...")
        Ball = nil
        return false
    end
end

-- Atualiza o Character e HumanoidRootPart quando o jogador renasce
LocalPlayer.CharacterAdded:Connect(function(newCharacter)
    Character = newCharacter
    HumanoidRootPart = newCharacter:WaitForChild("HumanoidRootPart")
    print("Personagem atualizado!")
end)

-- Função para pressionar F
local function PressF()
    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.F, false, game)
    wait()
    VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.F, false, game)
    print("Tecla F pressionada!")
end

-- Função para spam F
local function SpamF()
    print("Iniciando spam de F...")
    for i = 1, 5 do
        if not (Toggle1Enabled or Toggle2Enabled or Toggle3Enabled) then break end
        PressF()
        wait(0.1)
    end
end

-- Toggles
local Toggle1Enabled = false
local Toggle2Enabled = false
local Toggle3Enabled = false

-- Toggle 1: Auto-Parry baseado em distância e velocidade
local Toggle1 = Tab1:AddToggle({
    Name = "Auto-Parry 1",
    Description = "Baseado em distância e velocidade da bola",
    Default = false
})

Toggle1:Callback(function(Value)
    Toggle1Enabled = Value
    if Toggle1Enabled then
        print("Auto-Parry 1 ativado! Monitorando a bola...")
        FindBall()
    else
        print("Auto-Parry 1 desativado!")
    end
end)

-- Constantes para Toggle 1
local DETECTION_DISTANCE_1 = 20
local BALL_SPEED_THRESHOLD_1 = 5

local function IsBallCloseAndComingToggle1()
    if not Ball or not Ball.Parent or not HumanoidRootPart then return false, false end
    local distance = (Ball.Position - HumanoidRootPart.Position).Magnitude
    local ballVelocity = Ball:FindFirstChild("BodyVelocity") and Ball.BodyVelocity.MaxForce or (Ball.Velocity or Vector3.new(0, 0, 0))
    local directionToPlayer = (HumanoidRootPart.Position - Ball.Position).Unit
    local speedTowardsPlayer = ballVelocity:Dot(directionToPlayer)
    print("Toggle 1 - Distância:", distance, "Velocidade na direção:", speedTowardsPlayer)
    return distance <= DETECTION_DISTANCE_1, speedTowardsPlayer > BALL_SPEED_THRESHOLD_1
end

-- Toggle 2: Auto-Parry baseado em eventos do jogo
local Toggle2 = Tab1:AddToggle({
    Name = "Auto-Parry 2",
    Description = "Baseado em eventos do jogo",
    Default = false
})

Toggle2:Callback(function(Value)
    Toggle2Enabled = Value
    if Toggle2Enabled then
        print("Auto-Parry 2 ativado! Monitorando eventos...")
        FindBall()
    else
        print("Auto-Parry 2 desativado!")
    end
end)

-- Toggle 2: Lógica baseada em eventos (simplificado, já que não temos eventos específicos)
local DETECTION_DISTANCE_2 = 15
local function IsBallCloseToggle2()
    if not Ball or not Ball.Parent or not HumanoidRootPart then return false end
    local distance = (Ball.Position - HumanoidRootPart.Position).Magnitude
    print("Toggle 2 - Distância:", distance)
    return distance <= DETECTION_DISTANCE_2
end

-- Toggle 3: Auto-Parry baseado apenas em distância
local Toggle3 = Tab1:AddToggle({
    Name = "Auto-Parry 3",
    Description = "Baseado apenas em distância",
    Default = false
})

Toggle3:Callback(function(Value)
    Toggle3Enabled = Value
    if Toggle3Enabled then
        print("Auto-Parry 3 ativado! Monitorando a bola...")
        FindBall()
    else
        print("Auto-Parry 3 desativado!")
    end
end)

-- Constantes para Toggle 3
local DETECTION_DISTANCE_3 = 25

local function IsBallCloseToggle3()
    if not Ball or not Ball.Parent or not HumanoidRootPart then return false end
    local distance = (Ball.Position - HumanoidRootPart.Position).Magnitude
    print("Toggle 3 - Distância:", distance)
    return distance <= DETECTION_DISTANCE_3
end

-- Loop para tentar encontrar a bola continuamente
RunService.Heartbeat:Connect(function()
    if (Toggle1Enabled or Toggle2Enabled or Toggle3Enabled) and not Ball then
        FindBall()
    end
end)

-- Loop principal para os toggles
RunService.Heartbeat:Connect(function()
    if not Ball or not Ball.Parent or not HumanoidRootPart then return end

    -- Toggle 1
    if Toggle1Enabled then
        local isClose, isComing = IsBallCloseAndComingToggle1()
        if isClose and isComing then
            PressF()
        end
    end

    -- Toggle 2
    if Toggle2Enabled then
        local isClose = IsBallCloseToggle2()
        if isClose then
            PressF()
        end
    end

    -- Toggle 3
    if Toggle3Enabled then
        local isClose = IsBallCloseToggle3()
        if isClose then
            SpamF()
        end
    end
end)

-- Detectar clique na tela
UserInputService.InputBegan:Connect(function(input, gameProcessedEvent)
    if not (Toggle1Enabled or Toggle2Enabled or Toggle3Enabled) then return end
    if gameProcessedEvent then return end
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        PressF()
    end
end)
