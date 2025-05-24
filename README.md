local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()

-- KeyGuardian Config
local KeyGuardLibrary = loadstring(game:HttpGet("https://cdn.keyguardian.org/library/v1.0.0.lua"))()
local trueData = "83bf4edd89dd485382a118f2922766bc"
local falseData = "7fa5a51db19844a1b896bab0e1a49a08"

KeyGuardLibrary.Set({
    publicToken = "de3a1a7a25884f2a94a564f0c23cee6c",
    privateToken = "3d87829343784d35b8e898ac05e42197",
    trueData = trueData,
    falseData = falseData,
})

-- Criar janela principal
local Window = redzlib:MakeWindow({
    Title = "Coquette Hub 3.6",
    SubTitle = "by Lolytadev 💖",
    SaveFolder = "coquette_key",
})

Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://135441295532401", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

-- Aba de Key System
local KeyTab = Window:MakeTab({"🔑 Key System", "Chave de acesso"})

local key = ""

KeyTab:AddTextBox({
    Name = "Digite sua Key",
    Description = "Cole sua key válida aqui",
    PlaceholderText = "ex: my-key-123",
    Callback = function(Value)
        key = Value
    end
})

KeyTab:AddButton({"✅ Verificar Key", function()
    local response = KeyGuardLibrary.validateDefaultKey(key)
    if response == trueData then
        print("✅ Key válida!")
        
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Daivd977/Deivd999/refs/heads/main/pessal"))()

        game.StarterGui:SetCore("SendNotification", {
            Title = "Coquette Hub",
            Text = "Key válida! Acesso liberado!",
            Duration = 5
        })

        -- Exemplo de criar nova aba funcional:
        local MainTab = Window:MakeTab({"🏠 Principal", "Scripts e Funções"})
        MainTab:AddButton({"Print", function() print("Script liberado!") end})

    else
        print("❌ Key inválida.")
        game.StarterGui:SetCore("SendNotification", {
            Title = "Erro",
            Text = "Key inválida, tente novamente!",
            Duration = 4
        })
    end
end})

KeyTab:AddButton({"📋 Obter Key", function()
    setclipboard(KeyGuardLibrary.getLink())
    game.StarterGui:SetCore("SendNotification", {
        Title = "Link copiado!",
        Text = "Cole no navegador para obter a key",
        Duration = 5
    })
end})
