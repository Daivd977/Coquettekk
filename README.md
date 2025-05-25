local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local CoreGui = game:GetService("CoreGui")
local StarterGui = game:GetService("StarterGui")
local RunService = game:GetService("RunService")

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
    Title = "Coquette Hub 3.634235235",
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
local LastHitTime = 0 -- Para controlar o cooldown
local COOLDOWN = 0.5 -- Tempo de espera entre disparos do evento (em segundos)

-- Atualiza o Character e HumanoidRootPart quando o jogador renasce
LocalPlayer.CharacterAdded:Connect(function(newCharacter)
    Character = newCharacter
    HumanoidRootPart = newCharacter:WaitForChild("HumanoidRootPart")
    print("Personagem atualizado!")
end)

-- Função para bater na bola usando o evento remoto
local function HitBall()
    -- Verifica o cooldown
    local currentTime = tick()
    if currentTime - LastHitTime < COOLDOWN then
        print("Cooldown ativo, esperando...")
        return
    end

    -- Monta os argumentos para o evento remoto
    local args = {
        [2] = "Ep1adq", -- Identificador da ação
        [3] = HumanoidRootPart.CFrame, -- Posição/orientação do jogador
        [4] = HumanoidRootPart.CFrame, -- Usamos a mesma posição do jogador, já que não estamos detectando a bola
        [5] = false -- Booleano (mantido como false, como no exemplo)
    }

    -- Dispara o evento remoto
    pcall(function()
        game:GetService("CookiesService"):WaitForChild("\n"):FireServer(unpack(args))
        print("Evento remoto disparado para bater na bola!")
        LastHitTime = tick() -- Atualiza o tempo do último disparo
    end)
end

-- Toggle
local ToggleEnabled = false

local Toggle = Tab1:AddToggle({
    Name = "Spam Hit",
    Description = "Ativa o spam para bater na bola",
    Default = false
})

Toggle:Callback(function(Value)
    ToggleEnabled = Value
    if ToggleEnabled then
        print("Spam Hit ativado!")
    else
        print("Spam Hit desativado!")
    end
end)

-- Loop principal para o spam
RunService.Heartbeat:Connect(function()
    if not ToggleEnabled then return end
    if not HumanoidRootPart then return end

    print("Tentando bater na bola (spam)...")
    HitBall()
end)
