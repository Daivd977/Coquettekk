--blade ball



local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local CoreGui = game:GetService("CoreGui")
local StarterGui = game:GetService("StarterGui")
local lp = Players.LocalPlayer

-- Função que cria a tela de loading e retorna uma promise
local function createLoadingScreen()
    local promise = {}
    promise.completed = false
    promise.connection = nil
    
    -- Remove GUI antiga se existir
    pcall(function()
        if CoreGui:FindFirstChild("LoadingScreen") then
            CoreGui.LoadingScreen:Destroy()
        end
    end)

    -- Cria a UI de carregamento
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

    -- Animação da barra de carregamento
    local tween = TweenService:Create(
        bar,
        TweenInfo.new(4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
        {Size = UDim2.new(1, 0, 1, 0)}
    )
    tween:Play()

    -- Função para limpar a UI
    local function cleanup()
        if gui then
            gui:Destroy()
        end
        if promise.connection then
            promise.connection:Disconnect()
        end
    end

    -- Após a barra carregar, faz o fade out e destrói a UI
    promise.connection = tween.Completed:Connect(function()
        -- Fade out suave da UI
        TweenService:Create(frame, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(barBG, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(bar, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 1}):Play()
        TweenService:Create(image, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {ImageTransparency = 1}):Play()
        TweenService:Create(nameText, TweenInfo.new(1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {TextTransparency = 1}):Play()
        
        -- Aguarda o fade out terminar
        task.delay(1.2, function()
            -- Toca som de conclusão
            local sound = Instance.new("Sound")
            sound.SoundId = "rbxassetid://8486683243"
            sound.Volume = 0.5
            sound.PlayOnRemove = true
            sound.Parent = workspace
            sound:Destroy()
            
            -- Exibe a notificação de boas-vindas
            StarterGui:SetCore("SendNotification", {
                Title = "Coquette Hub",
                Text = "Bem-vindo à Coquette Hub 💖",
                Duration = 4
            })
            
            -- Marca como concluído e limpa
            promise.completed = true
            cleanup()
        end)
    end)
    
    return promise
end

-- Função para esperar até que a promise seja resolvida
local function waitForPromise(promise)
    while not promise.completed do
        task.wait()
    end
end

-- Uso:
local loadingPromise = createLoadingScreen()

-- Aqui você coloca o código que deve esperar até que o loading termine
waitForPromise(loadingPromise)

-- SEU CÓDIGO ABAIXO AQUI
print("Loading completo! Agora executando o resto do script...")
-- ... resto do seu código ...

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



local Tab1 = Window:MakeTab({"Credits", "info"})


local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")
local VirtualInputManager = game:GetService("VirtualInputManager")

local LocalPlayer = Players.LocalPlayer
local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
local Ball = workspace.Map.Grassy_Classic.Border.BallFloor

-- Constantes
local DETECTION_DISTANCE = 15
local PLAYER_DETECTION_DISTANCE = 20
local BALL_SPEED_THRESHOLD = 10

-- Estado do toggle
local ToggleEnabled = false

-- Função para pressionar F
local function PressF()
    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.F, false, game)
    wait()
    VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.F, false, game)
end

-- Função para spam F
local function SpamF()
    for i = 1, 5 do
        if not ToggleEnabled then break end
        PressF()
        wait(0.1)
    end
end

-- Verifica se a bola está perto e vindo na sua direção
local function IsBallCloseAndComing()
    if not Ball or not HumanoidRootPart then return false, false end
    local distance = (Ball.Position - HumanoidRootPart.Position).Magnitude
    local ballVelocity = Ball.Velocity
    local directionToPlayer = (HumanoidRootPart.Position - Ball.Position).Unit
    local speedTowardsPlayer = ballVelocity:Dot(directionToPlayer)
    return distance <= DETECTION_DISTANCE, speedTowardsPlayer > BALL_SPEED_THRESHOLD
end

-- Verifica se outro jogador está perto e batendo na bola
local function IsOtherPlayerCloseAndHitting()
    for _, player in pairs(Players:GetPlayers()) do
        if player ~= LocalPlayer and player.Character then
            local otherCharacter = player.Character
            local otherRootPart = otherCharacter:FindFirstChild("HumanoidRootPart")
            if otherRootPart then
                local distanceToOtherPlayer = (otherRootPart.Position - HumanoidRootPart.Position).Magnitude
                if distanceToOtherPlayer <= PLAYER_DETECTION_DISTANCE then
                    local _, isComing = IsBallCloseAndComing()
                    if isComing then
                        return true
                    end
                end
            end
        end
    end
    return false
end


local Toggle1 = Tab1:AddToggle({
    Name = "Toggle",
    Description = "This is a <font color='rgb(88, 101, 242)'>Toggle</font> Example",
    Default = false
})

Toggle1:Callback(function(Value)
    ToggleEnabled = Value
    if ToggleEnabled then
        print("Toggle ativado! Monitorando a bola...")
    else
        print("Toggle desativado!")
    end
end)

-- Loop principal
RunService.Heartbeat:Connect(function()
    if not ToggleEnabled then return end
    if not Ball or not HumanoidRootPart then return end

    local isClose, isComing = IsBallCloseAndComing()
    local otherPlayerHitting = IsOtherPlayerCloseAndHitting()

    if isClose and isComing then
        if otherPlayerHitting then
            SpamF()
        else
            PressF()
        end
    end
end)

-- Detectar clique na tela
UserInputService.InputBegan:Connect(function(input, gameProcessedEvent)
    if not ToggleEnabled then return end
    if gameProcessedEvent then return end
    if input.UserInputType == Enum.UserInputType.MouseButton1 then
        PressF()
    end
end)
