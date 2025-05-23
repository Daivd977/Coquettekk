
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


-- Adicionar seção de personalização da UI
local CustomizeSection = Tab1:AddSection({"Personalização da UI"})

-- Função auxiliar para aplicar tema
local function ApplyTheme(theme)
    local themeSettings = {
        Claro = {BackgroundColor = Color3.fromRGB(240, 240, 240), TextColor = Color3.fromRGB(0, 0, 0), BorderColor = Color3.fromRGB(100, 100, 100)},
        Escuro = {BackgroundColor = Color3.fromRGB(30, 30, 30), TextColor = Color3.fromRGB(255, 255, 255), BorderColor = Color3.fromRGB(80, 80, 80)},
        Neon = {BackgroundColor = Color3.fromRGB(0, 0, 0), TextColor = Color3.fromRGB(0, 255, 255), BorderColor = Color3.fromRGB(0, 255, 0)}
    }
    local settings = themeSettings[theme] or themeSettings.Claro
    for _, uiElement in pairs(redzlib.UIElements) do
        if uiElement:IsA("GuiObject") then
            uiElement.BackgroundColor3 = settings.BackgroundColor
            uiElement.TextColor3 = settings.TextColor
            if uiElement:IsA("Frame") or uiElement:IsA("TextButton") then
                uiElement.BorderColor3 = settings.BorderColor
            end
        end
    end
end

-- Dropdown para selecionar tema
local ThemeDropdown = CustomizeSection:AddDropdown({
    Name = "Tema da UI",
    Description = "Escolha um <font color='rgb(88, 101, 242)'>tema</font> para a interface",
    Options = {"Claro", "Escuro", "Neon"},
    Default = "Claro",
    Flag = "ui_theme",
    Callback = function(Value)
        ApplyTheme(Value)
    end
})

-- Seletor de cor de fundo (simulado com sliders RGB)
CustomizeSection:AddSlider({
    Name = "Cor de Fundo (R)",
    Min = 0,
    Max = 255,
    Increase = 1,
    Default = 240,
    Callback = function(Value)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("GuiObject") then
                local currentColor = uiElement.BackgroundColor3
                uiElement.BackgroundColor3 = Color3.fromRGB(Value, currentColor.G * 255, currentColor.B * 255)
            end
        end
    end
})
CustomizeSection:AddSlider({
    Name = "Cor de Fundo (G)",
    Min = 0,
    Max = 255,
    Increase = 1,
    Default = 240,
    Callback = function(Value)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("GuiObject") then
                local currentColor = uiElement.BackgroundColor3
                uiElement.BackgroundColor3 = Color3.fromRGB(currentColor.R * 255, Value, currentColor.B * 255)
            end
        end
    end
})
CustomizeSection:AddSlider({
    Name = "Cor de Fundo (B)",
    Min = 0,
    Max = 255,
    Increase = 1,
    Default = 240,
    Callback = function(Value)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("GuiObject") then
                local currentColor = uiElement.BackgroundColor3
                uiElement.BackgroundColor3 = Color3.fromRGB(currentColor.R * 255, currentColor.G * 255, Value)
            end
        end
    end
})

-- Slider para transparência
CustomizeSection:AddSlider({
    Name = "Transparência da UI",
    Min = 0,
    Max = 1,
    Increase = 0.01,
    Default = 0,
    Callback = function(Value)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("GuiObject") then
                uiElement.BackgroundTransparency = Value
            end
        end
    end
})

-- Slider para tamanho da fonte
CustomizeSection:AddSlider({
    Name = "Tamanho da Fonte",
    Min = 12,
    Max = 24,
    Increase = 1,
    Default = 14,
    Callback = function(Value)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("TextLabel") or uiElement:IsA("TextButton") or uiElement:IsA("TextBox") then
                uiElement.TextSize = Value
            end
        end
    end
})

-- Dropdown para estilo de borda
CustomizeSection:AddDropdown({
    Name = "Estilo de Borda",
    Description = "Escolha o <font color='rgb(88, 101, 242)'>estilo</font> das bordas",
    Options = {"Arredondado", "Quadrado", "Sem Borda"},
    Default = "Arredondado",
    Flag = "ui_border_style",
    Callback = function(Value)
        local cornerRadius = Value == "Arredondado" and UDim.new(0, 8) or UDim.new(0, 0)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("Frame") or uiElement:IsA("TextButton") then
                local uiCorner = uiElement:FindFirstChildOfClass("UICorner") or Instance.new("UICorner")
                uiCorner.CornerRadius = cornerRadius
                uiCorner.Parent = uiElement
            end
            if Value == "Sem Borda" then
                uiElement.BorderSizePixel = 0
            else
                uiElement.BorderSizePixel = 1
            end
        end
    end
})

-- Toggle para animações
CustomizeSection:AddToggle({
    Name = "Animações da UI",
    Description = "Ativa/desativa <font color='rgb(88, 101, 242)'>animações</font> suaves",
    Default = true,
    Callback = function(Value)
        redzlib.Flags.EnableUIAnimations = Value
        -- Lógica de animação pode ser implementada aqui (ex.: TweenService)
        for _, uiElement in pairs(redzlib.UIElements) do
            if uiElement:IsA("GuiObject") then
                if Value then
                    -- Exemplo: adicionar transição suave ao mudar visibilidade
                    local tweenInfo = TweenInfo.new(0.3, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)
                    local tween = game:GetService("TweenService"):Create(uiElement, tweenInfo, {Transparency = uiElement.BackgroundTransparency})
                    tween:Play()
                else
                    -- Remover animações (alterações instantâneas)
                    uiElement.Transparency = uiElement.BackgroundTransparency
                end
            end
        end
    end
})

-- Inicializar flags
redzlib.Flags.EnableUIAnimations = true
redzlib.Flags.UITheme = "Claro"
redzlib.Flags.UIBorderStyle = "Arredondado"

-- Manter os elementos originais fornecidos
local Section = Tab1:AddSection({"Section"})
Tab1:AddButton({"Print", function(Value)
    print("Hello World!")
end})

local Toggle1 = Tab1:AddToggle({
    Name = "Toggle",
    Description = "This is a <font color='rgb(88, 101, 242)'>Toggle</font> Example",
    Default = false
})
Toggle1:Callback(function(Value)
    -- Manter o callback original
end)

Tab1:AddSlider({
    Name = "Speed",
    Min = 1,
    Max = 100,
    Increase = 1,
    Default = 16,
    Callback = function(Value)
        -- Manter o callback original
    end
})

local Dropdown = Tab1:AddDropdown({
    Name = "Players List",
    Description = "Select the <font color='rgb(88, 101, 242)'>Number</font>",
    Options = {"one", "two", "three"},
    Default = "two",
    Flag = "dropdown teste",
    Callback = function(Value)
        -- Manter o callback original
    end
})

Tab1:AddTextBox({
    Name = "Name item",
    Description = "1 Item on 1 Server",
    PlaceholderText = "item only",
    Callback = function(Value)
        -- Manter o callback original
    end
})
