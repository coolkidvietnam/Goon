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
    local gui = player:WaitForChild("PlayerGui")

    for _, descendant in pairs(gui:GetDescendants()) do
        if descendant:IsA("TextLabel") or descendant:IsA("TextButton") then
            if string.find(descendant.Text:lower(), "yerk off") then
                descendant.Text = "sục"
            end
        end
    end
end
