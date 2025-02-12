local Players = game:GetService("Players")
local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")

local player = Players.LocalPlayer
local mouse = player:GetMouse()
local camera = workspace.CurrentCamera

-- Configurações
local enabled = false
local fov = 200 -- Ajuste o FOV conforme necessário
local key = Enum.KeyCode.P

-- Interface do usuário
local gui = Instance.new("ScreenGui")
local status = Instance.new("TextLabel")
gui.Parent = player.PlayerGui

status.Size = UDim2.new(0, 200, 0, 50)
status.Position = UDim2.new(0.8, 0, 0, 0)
status.BackgroundTransparency = 0.5
status.TextColor3 = Color3.new(1, 1, 1)
status.Parent = gui

-- Função principal do aimbot
local function getClosestEnemy()
    local closest = nil
    local maxDist = fov
    
    for _, otherPlayer in pairs(Players:GetPlayers()) do
        if otherPlayer ~= player and otherPlayer.Team ~= player.Team then
            local character = otherPlayer.Character
            if character▍
