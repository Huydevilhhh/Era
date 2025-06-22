local args = {
	1
}
game:GetService("ReplicatedStorage"):WaitForChild("GameEvents"):WaitForChild("BuyPetEgg"):FireServer(unpack(args))
wait()
local args = {
	2
}
game:GetService("ReplicatedStorage"):WaitForChild("GameEvents"):WaitForChild("BuyPetEgg"):FireServer(unpack(args))
wait()
local args = {
	3
}
game:GetService("ReplicatedStorage"):WaitForChild("GameEvents"):WaitForChild("BuyPetEgg"):FireServer(unpack(args))
wait(1.2)
local itemName = "Paradise Egg x1" -- Tên chính xác của món đồ

local player = game.Players.LocalPlayer
local backpack = player:WaitForChild("Backpack")
local function getCharacter()
    return player.Character or player.CharacterAdded:Wait()
end

-- Hàm để cầm món đồ
local function equipItem()
    local character = getCharacter()
    local tool = backpack:FindFirstChild(itemName)
    if tool then
        tool.Parent = character
        print("Đã cầm món đồ:", itemName)
    else
        warn("Không tìm thấy món đồ:", itemName)
    end
end

-- Gọi hàm khi load nhân vật hoặc sau vài giây
player.CharacterAdded:Connect(function()
    wait(1)
    equipItem()
end)

-- Nếu nhân vật đã có sẵn thì gọi luôn
if player.Character then
    wait(1)
    equipItem()
end
