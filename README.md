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

    for _, tool in pairs(backpack:GetChildren()) do
        if tool:IsA("Tool") and string.lower(tool.Name) == "jerk off" then
            tool.Name = "sục"
        end
    end
end
