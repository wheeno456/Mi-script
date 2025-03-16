-- carregar biblioteca
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()

local Window = Fluent:CreateWindow({
    Title = "Universal scripts" .. Fluent.Version,
    TabWidth = 160, Size = UDim2.fromOffset(580, 460), Theme = "Dark"
})

local Tabs = {
    Main = Window:AddTab({ Title = "Scripts" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}
-- parágrafos
Tabs.Main:AddParagraph({ Title = "feito por loadstringzxc", Content = "Scripts abaixo" })
-- botoes
Tabs.Main:AddButton({ Title = "fly gui v3 (se ele vier ja executado é bug)", Callback = function() 
end })
loadstring(game:HttpGet("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))()
Tabs.Main:AddButton({ Title = "Esp e aimbot", Callback = function() 
loadstring(game:HttpGet('https://raw.githubusercontent.com/fatesc/fates-esp/main/main.lua'))()
end })
Tabs.Main:AddButton({ Title = "Button", Callback = function() 
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end })


local Toggle = Tabs.Main:AddToggle("MyToggle", { Title = "Toggle" })
Toggle:OnChanged(function() print(Options.MyToggle.Value) end)
