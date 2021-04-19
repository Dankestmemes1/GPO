local library = loadstring(game.HttpGet(game, 'https://pastebin.com/raw/vGwikY93'))()

local w1 = library:Window('GPO') -- Text



w1:Toggle('Toggle Train', 'haki', false, function(toggled)
    getgenv().autofarm = toggled;

while wait() do
  if getgenv().autofarm == toggled then
  
   local args = {
    [1] = "Buso"
}

game:GetService("ReplicatedStorage").Events.Haki:FireServer(unpack(args))

   wait(60)

  end
    end


end) -- Text, Flag, Enabled, Callback, Flag Location (Optional)

w1:Label('Train Haki ez') -- Text

w1:Button('Destroy GUI', function()
    for i,v in pairs(game.CoreGui:GetChildren()) do
        if v:FindFirstChild('Top') then
            v:Destroy()    
        end
    end
end) -- Text, Callback


