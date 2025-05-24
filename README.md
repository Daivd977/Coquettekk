local KeyGuardLibrary = loadstring(game:HttpGet("https://cdn.keyguardian.org/library/v1.0.0.lua"))()
local trueData = "783e5055a50444c8bd0e5bc59453de68"
local falseData = "5da489bfd9334c26a9c5013f1a85d149"

KeyGuardLibrary.Set({
	publicToken = "de3a1a7a25884f2a94a564f0c23cee6c",
	privateToken = "3d87829343784d35b8e898ac05e42197",
	trueData = trueData,
	falseData = falseData,
})

local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/tbao143/Library-ui/refs/heads/main/Redzhubui"))()

local key = ""

local Window = redzlib:MakeWindow({
    Title = "Coquette Hub 3.6",
    SubTitle = "by Lolytadev 💖",
    SaveFolder = "CoquetteKey"
})

Window:AddMinimizeButton({
    Button = { Image = "rbxassetid://135441295532401", BackgroundTransparency = 0 },
    Corner = { CornerRadius = UDim.new(35, 1) },
})

local Tab1 = Window:MakeTab({"🔑 Key System", "Validation"})

-- Caixa de texto para digitar a key
Tab1:AddTextBox({
  Name = "Enter Key",
  Description = "Paste your access key here.",
  PlaceholderText = "Ex: ABCD-EFGH-1234",
  Callback = function(Value)
    key = Value
  end
})

-- Botão para checar a key
Tab1:AddButton({"✅ Check Key", function()
  local response = KeyGuardLibrary.validateDefaultKey(key)
  if response == trueData then
    print("✅ Key is valid!")
    

loadstring(game:HttpGet("https://raw.githubusercontent.com/Daivd977/Deivd999/refs/heads/main/pessal"))()



  else
    warn("❌ Invalid key!")
  end
end})

-- Botão para copiar o link da key
Tab1:AddButton({"🔗 Get Key Link", function()
  setclipboard(KeyGuardLibrary.getLink())
  print("🔗 Key link copied to clipboard!")
end})
