repeat wait() until game:IsLoaded()
wait(10)
local vu = game:GetService("VirtualUser")
game:GetService("Players").LocalPlayer.Idled:connect(function()
   vu:Button2Down(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
   wait(1)
   vu:Button2Up(Vector2.new(0,0),workspace.CurrentCamera.CFrame)
end)
if game.PlaceId == 11040063484 then -- XMAS-Sword-Fighters-Simulator
 

local DiscordLib = loadstring(game:HttpGet("https://pastebin.com/raw/xcdmdnw0"))()
local win = DiscordLib:Window("XMAS-Sword-Fighters-Simulator")

local serv = win:Server("PNonShopByPFN", "")



local tgls = serv:Channel("AutoFarm")
--local tgls1 = serv:Channel("Egg")
--local tgls2 = serv:Channel("TP")
--local tgls3 = serv:Channel("TP Event Power")
---------------------------------------------------------------------------

_G.Click = true
_G.PowerTrain = true

_G.RankUp = true

----------------------------------------------------------------------------


tgls:Toggle("ClickAFK",true, function(bool)
    _G.Click = bool
end)

tgls:Toggle("PowerTrain",true, function(bool)
    _G.PowerTrain = bool
end)

tgls:Toggle("RankUp",true, function(bool)
    _G.RankUp = bool
end)


----------------------------------------------------------------------------

local ViSendMouseButtonEvent = game:service'VirtualInputManager'

spawn(function()
    while wait() do
      if _G.Click then
        pcall(function()
            ViSendMouseButtonEvent:SendMouseButtonEvent(795, 595, 0, true, game, 1)
wait(0.5)
ViSendMouseButtonEvent:SendMouseButtonEvent(795, 595, 0, false, game, 1)    
            
        end)
      end
    end
end)
-----------------------------------------------------------------------------


spawn(function()
    while wait() do
      if _G.PowerTrain then
        pcall(function() 
            


local args = {
    [1] = {
        [1] = "PowerTrain"
    }
}


game:GetService("ReplicatedStorage").Packages.Knit.Services.ClickService.RF.Click:InvokeServer()



 
            wait()
            
            
        end)
      end
    end
end)
-------

_G.MAGNET = true
tgls:Toggle("MAGNET",true, function(bool)
  _G.MAGNET = bool
end)
spawn(function()
  while wait(0.1) do
    if _G.MAGNET then
      pcall(function() 
          


        local Coin = game.Players.localPlayer.Character.HumanoidRootPart
        for i,v in pairs(game.Workspace.Live.Pickups:GetChildren()) do
            v.CFrame = Coin.CFrame
            wait()
            end
    
           
          
      end)
    end
  end
end)
-----

------

spawn(function()
    while wait(14.1) do
      if _G.RankUp then
        pcall(function() 
            



local args = {
    [1] = {
        [1] = "RankUp"
    }
}


game:GetService("ReplicatedStorage").Packages.Knit.Services.AscendService.RF.Ascend:InvokeServer()



 
            wait()
            
            
        end)
      end
    end
end)





    end
