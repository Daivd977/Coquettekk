local v8 = loadstring(game:HttpGet('https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua'))();
local v9 = v8:CreateWindow({
    Title = 'NEOX HUB | FISCHv1.5',
    SubTitle = 'by hassanxzayn',
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = false,
    Theme = 'Darker',
    MinimizeKey = Enum.KeyCode.LeftControl
});
local v10 = {
    Home = v9:AddTab({
        Title = '| Home',
        Icon = 'rbxassetid://7733960981'
    }),
    Main = v9:AddTab({
        Title = '| Main',
        Icon = 'rbxassetid://7743869612'
    }),
    Misc = v9:AddTab({
        Title = '| Misc',
        Icon = 'rbxassetid://7733789088'
    }),
    Weather = v9:AddTab({
        Title = '| Environment Settings',
        Icon = 'rbxassetid://7734068495'
    }),
    Teleport = v9:AddTab({
        Title = '| Teleport',
        Icon = 'rbxassetid://7733992789'
    }),
    Performance = v9:AddTab({
        Title = '| Performance',
        Icon = 'rbxassetid://7733955511'
    }),
    ESP = v9:AddTab({
        Title = '| Esp',
        Icon = 'rbxassetid://7743876054'
    }),
    STATS = v9:AddTab({
        Title = '| Player And Sever Stats',
        Icon = 'rbxassetid://7743866778'
    }),
    info = v9:AddTab({
        Title = '| Info',
        Icon = 'rbxassetid://7733964719'
    })
};
v9:SelectTab(1);
v10.Home:AddButton({
    Title = 'Join our discord',
    Description = 'Click on this button to copy the invite link!',
    Callback = function()
        local v156 = 'https://discord.gg/99UuEwM9sX';
        if setclipboard then
            local v381 = 0;
            while true do
                if (v381 == 0) then
                    setclipboard(v156);
                    print('bro coming to our discord yay!');
                    break
                end
            end
        else
            print('setclipboard function not available');
        end
    end
});
AnalyticsService = game:GetService('AnalyticsService');
CollectionService = game:GetService('CollectionService');
DataStoreService = game:GetService('DataStoreService');
HttpService = game:GetService('HttpService');
Lighting = game:GetService('Lighting');
MarketplaceService = game:GetService('MarketplaceService');
Players = game:GetService('Players');
ReplicatedFirst = game:GetService('ReplicatedFirst');
ReplicatedStorage = game:GetService('ReplicatedStorage');
RunService = game:GetService('RunService');
ServerScriptService = game:GetService('ServerScriptService');
ServerStorage = game:GetService('ServerStorage');
SoundService = game:GetService('SoundService');
StarterGui = game:GetService('StarterGui');
StarterPack = game:GetService('StarterPack');
StarterPlayer = game:GetService('StarterPlayer');
TeleportService = game:GetService('TeleportService');
TweenService = game:GetService('TweenService');
Teams = game:GetService('Teams');
VirtualUser = game:GetService('VirtualUser');
Workspace = game:GetService('Workspace');
UserInputService = game:GetService('UserInputService');
VirtualInputManager = game:GetService('VirtualInputManager');
ContextActionService = game:GetService('ContextActionService');
GuiService = game:GetService('GuiService');
print('ClientMonsterTools.lua loaded');
local v11 = Players.LocalPlayer;
local v12 = v11.Character;
local v13 = v12:FindFirstChild('HumanoidRootPart');
local v14 = Workspace:FindFirstChild('active');
local v15 = v11:FindFirstChildOfClass('PlayerGui');
local v16 = false;
local v17 = false;
local v18 = false;
local v19 = false;
local v20 = false;
local v21 = false;
local v22 = 0.3;
local v23 = false;
local v24 = false;
local v25 = false;
local v26 = false;
local v27 = false;
local v28 = false;
local v29 = false;
local v30 = false;
local v31 = Enum.KeyCode.F;
v15.ChildAdded:Connect(function(v157)
    if v157:IsA('ScreenGui') then
        if ((v157.Name == 'reel') and v23) then
            local v500 = 0;
            local v501;
            while true do
                if (v500 == (0)) then
                    v501 = ReplicatedStorage:WaitForChild('events'):WaitForChild('reelfinished');
                    if v501 then
                        while v157 do
                            local v750 = 0;
                            while true do
                                if (v750 == 0) then
                                    task.wait(2);
                                    v501:FireServer(100, false);
                                    break
                                end
                            end
                        end
                    end
                    break
                end
            end
        end
    end
end);
function AutoFish5()
    if v20 then
        task.spawn(function()
            while v18 do
                local v502 = 0;
                local v503;
                local v504;
                while true do
                    if (v502 == (0)) then
                        v503 = game:GetService('Players').LocalPlayer:WaitForChild('PlayerGui');
                        v504 = v503:FindFirstChild('shakeui');
                        v502 = 1;
                    end
                    if (v502 == (1)) then
                        if (v504 and v504.Enabled) then
                            local v730 = 0;
                            local v731;
                            while true do
                                if (v730 == 0) then
                                    v731 = v504:FindFirstChild('safezone');
                                    if v731 then
                                        local v821 = v731:FindFirstChild('button');
                                        if (v821 and v821:IsA('ImageButton') and v821.Visible) then
                                            if v17 then
                                                local v858 = 0;
                                                local v859;
                                                local v860;
                                                while true do
                                                    if (v858 == 1) then
                                                        VirtualInputManager:SendMouseButtonEvent(v859.X + (v860.X / (2)), v859.Y + (v860.Y / (2)), 0, true, game:GetService('Players').LocalPlayer, 0);
                                                        VirtualInputManager:SendMouseButtonEvent(v859.X + (v860.X / (2)), v859.Y + (v860.Y / 2), 0, false, game:GetService('Players').LocalPlayer, 0);
                                                        break
                                                    end
                                                    if (v858 == 0) then
                                                        local v877 = 0;
                                                        while true do
                                                            if (v877 == 0) then
                                                                v859 = v821.AbsolutePosition;
                                                                v860 = v821.AbsoluteSize;
                                                                v877 = 1;
                                                            end
                                                            if (v877 == (1)) then
                                                                v858 = 1;
                                                                break
                                                            end
                                                        end
                                                    end
                                                end
                                            elseif v19 then
                                                local v867 = 0;
                                                while true do
                                                    if (v867 == 0) then
                                                        GuiService.SelectedObject = v821;
                                                        VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game);
                                                        v867 = 1;
                                                    end
                                                    if (v867 == (1)) then
                                                        VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game);
                                                        break
                                                    end
                                                end
                                            end
                                        end
                                    end
                                    break
                                end
                            end
                        end
                        task.wait();
                        break
                    end
                end
            end
        end);
    else
        task.spawn(function()
            while v18 do
                local v505 = 0;
                local v506;
                local v507;
                while true do
                    if (v505 == 1) then
                        v507 = v506:FindFirstChild('shakeui');
                        if (v507 and v507.Enabled) then
                            local v732 = 0;
                            local v733;
                            while true do
                                if (v732 == 0) then
                                    v733 = v507:FindFirstChild('safezone');
                                    if v733 then
                                        local v822 = 0;
                                        local v823;
                                        while true do
                                            if (v822 == (0)) then
                                                v823 = v733:FindFirstChild('button');
                                                if (v823 and v823:IsA('ImageButton') and v823.Visible) then
                                                    if v17 then
                                                        local v878 = v823.AbsolutePosition;
                                                        local v879 = v823.AbsoluteSize;
                                                        VirtualInputManager:SendMouseButtonEvent(v878.X + (v879.X / (2)), v878.Y + (v879.Y / (2)), 0, true, game:GetService('Players').LocalPlayer, 0);
                                                        VirtualInputManager:SendMouseButtonEvent(v878.X + (v879.X / (2)), v878.Y + (v879.Y / (2)), 0, false, game:GetService('Players').LocalPlayer, 0);
                                                    elseif v19 then
                                                        local v884 = 0;
                                                        while true do
                                                            if ((0) == v884) then
                                                                GuiService.SelectedObject = v823;
                                                                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game);
                                                                v884 = 1;
                                                            end
                                                            if (v884 == (1)) then
                                                                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game);
                                                                break
                                                            end
                                                        end
                                                    end
                                                end
                                                break
                                            end
                                        end
                                    end
                                    break
                                end
                            end
                        end
                        break
                    end
                    if (v505 == 0) then
                        task.wait(v22);
                        v506 = game:GetService('Players').LocalPlayer:WaitForChild('PlayerGui');
                        v505 = 1;
                    end
                end
            end
        end);
    end
end
function ZoneCasting()
    if not ProtectPremium then
        return
    end
    spawn(function()
        while v21 do
            local v382 = 0;
            local v383;
            local v384;
            while true do
                if (v382 == (1)) then
                    if v384 then
                        local v618 = v384:FindFirstChildOfClass('Tool');
                        if v618 then
                            local v734 = v618:FindFirstChild('bobber');
                            if v734 then
                                local v760 = 0;
                                local v761;
                                local v762;
                                local v763;
                                while true do
                                    if (1 == v760) then
                                        v762 = Vector3.new(10, 1, 10);
                                        v763 = Vector3.new(0, - 4, 0);
                                        v760 = 2;
                                    end
                                    if (v760 == 0) then
                                        v761 = v734:FindFirstChild('RopeConstraint');
                                        if v761 then
                                            v761.Length = 2E5;
                                        end
                                        v760 = 1;
                                    end
                                    if (v760 == (2)) then
                                        if (selectedZoneCast == 'Bluefin Tuna Abundance') then
                                            local v847 = 0;
                                            local v848;
                                            while true do
                                                if (v847 == 0) then
                                                    v848 = Workspace.zones.fishing:FindFirstChild('Deep Ocean');
                                                    if v848 then
                                                        local v880 = v848:FindFirstChild('Abundance');
                                                        if (v880 and (v880.Value == 'Bluefin Tuna')) then
                                                            local v885 = 0;
                                                            local v886;
                                                            local v887;
                                                            local v888;
                                                            while true do
                                                                if (v885 == (1)) then
                                                                    v888 = nil;
                                                                    while true do
                                                                        if (v886 == 2) then
                                                                            v888.Position = v734.Position + v763 ;
                                                                            v888.Anchored = true;
                                                                            v886 = 3;
                                                                        end
                                                                        if (v886 == 0) then
                                                                            v887 = CFrame.new(v848.Position.X, 126.564, v848.Position.Z);
                                                                            v734.CFrame = v887;
                                                                            v886 = 1;
                                                                        end
                                                                        if (v886 == 1) then
                                                                            v888 = Instance.new('Part');
                                                                            v888.Size = v762;
                                                                            v886 = 2;
                                                                        end
                                                                        if ((4) == v886) then
                                                                            v888.Transparency = 1;
                                                                            break
                                                                        end
                                                                        if ((3) == v886) then
                                                                            v888.Parent = v734;
                                                                            v888.BrickColor = BrickColor.new('Bright blue');
                                                                            v886 = 4;
                                                                        end
                                                                    end
                                                                    break
                                                                end
                                                                if (v885 == 0) then
                                                                    v886 = 0;
                                                                    v887 = nil;
                                                                    v885 = 1;
                                                                end
                                                            end
                                                        end
                                                    end
                                                    break
                                                end
                                            end
                                        elseif (selectedZoneCast == 'Swordfish Abundance') then
                                            local v861 = 0;
                                            local v862;
                                            while true do
                                                if (v861 == (0)) then
                                                    v862 = Workspace.zones.fishing:FindFirstChild('Deep Ocean');
                                                    if v862 then
                                                        local v889 = v862:FindFirstChild('Abundance');
                                                        if (v889 and (v889.Value == 'Swordfish')) then
                                                            local v892 = CFrame.new(v862.Position.X, 126.564, v862.Position.Z);
                                                            v734.CFrame = v892;
                                                            local v894 = Instance.new('Part');
                                                            v894.Size = v762;
                                                            v894.Position = v734.Position + v763 ;
                                                            v894.Anchored = true;
                                                            v894.Parent = v734;
                                                            v894.BrickColor = BrickColor.new('Bright blue');
                                                            v894.Transparency = 1;
                                                        end
                                                    end
                                                    break
                                                end
                                            end
                                        else
                                            local v863 = Workspace.zones.fishing:FindFirstChild(selectedZoneCast);
                                            if v863 then
                                                local v868;
                                                if (selectedZoneCast == 'FischFright24') then
                                                    v868 = CFrame.new(v863.Position.X, 126, v863.Position.Z);
                                                elseif (selectedZoneCast == 'Isonade') then
                                                    v868 = CFrame.new(v863.Position.X, 126, v863.Position.Z);
                                                elseif (selectedZoneCast == 'Deep Ocean') then
                                                    v868 = CFrame.new(1521, 126, - 3543);
                                                elseif (selectedZoneCast == 'Desolate Deep') then
                                                    v868 = CFrame.new(- 1068, 126, - 3108);
                                                elseif (selectedZoneCast == 'Harvesters Spike') then
                                                    v868 = CFrame.new(- 1234, 126, 1748);
                                                elseif (selectedZoneCast == 'Moosewood Docks') then
                                                    v868 = CFrame.new(345, 126, 214);
                                                elseif (selectedZoneCast == 'Moosewood Ocean') then
                                                    v868 = CFrame.new(890, 126, 465);
                                                elseif (selectedZoneCast == 'Moosewood Ocean Mythical') then
                                                    v868 = CFrame.new(270, 126, 52);
                                                elseif (selectedZoneCast == 'Moosewood Pond') then
                                                    v868 = CFrame.new(526, 126, 305);
                                                elseif (selectedZoneCast == 'Mushgrove Water') then
                                                    v868 = CFrame.new(2541, 126, - 792);
                                                elseif (selectedZoneCast == 'Ocean') then
                                                    v868 = CFrame.new(- 5712, 126, 4059);
                                                elseif (selectedZoneCast == 'Roslit Bay') then
                                                    v868 = CFrame.new(- 1650, 126, 504);
                                                elseif (selectedZoneCast == 'Roslit Bay Ocean') then
                                                    v868 = CFrame.new(- 1825, 126, 946);
                                                elseif (selectedZoneCast == 'Roslit Pond') then
                                                    v868 = CFrame.new(- 1807, 141, 599);
                                                elseif (selectedZoneCast == 'Roslit Pond Seaweed') then
                                                    v868 = CFrame.new(- 1804, 141, 625);
                                                elseif (selectedZoneCast == 'Scallop Ocean') then
                                                    v868 = CFrame.new(16, 126, 730);
                                                elseif (selectedZoneCast == 'Snowcap Ocean') then
                                                    v868 = CFrame.new(2308, 126, 2200);
                                                elseif (selectedZoneCast == 'Snowcap Pond') then
                                                    v868 = CFrame.new(2777, 275, 2605);
                                                elseif (selectedZoneCast == 'Sunstone') then
                                                    v868 = CFrame.new(- 645, 126, - 955);
                                                elseif (selectedZoneCast == 'Terrapin Ocean') then
                                                    v868 = CFrame.new(- 57, 126, 2011);
                                                elseif (selectedZoneCast == 'The Arch') then
                                                    v868 = CFrame.new(1076, 126, - 1202);
                                                elseif (selectedZoneCast == 'Vertigo') then
                                                    v868 = CFrame.new(- 75, - 740, 12E2);
                                                end
                                                v734.CFrame = v868;
                                                local v870 = Instance.new('Part');
                                                v870.Size = v762;
                                                v870.Position = v734.Position + v763 ;
                                                v870.Anchored = true;
                                                v870.Parent = v734;
                                                v870.BrickColor = BrickColor.new('Bright blue');
                                                v870.Transparency = 1;
                                            end
                                        end
                                        break
                                    end
                                end
                            else
                                print('Bobber not found in the tool.');
                            end
                        else
                            print('No tool found in the character.');
                        end
                    end
                    task.wait(0.01);
                    break
                end
                if (v382 == (0)) then
                    v383 = game.Players.LocalPlayer;
                    v384 = v383.Character;
                    v382 = 1;
                end
            end
        end
    end);
end
function AntiAfk2()
    spawn(function()
        while v29 do
            local v385 = 0;
            while true do
                if (v385 == 0) then
                    game:GetService('ReplicatedStorage'):WaitForChild('events'):WaitForChild('afk'):FireServer(false);
                    task.wait(1E-2);
                    break
                end
            end
        end
    end);
end
v15.ChildAdded:Connect(function(v158)
    if v158:IsA('ScreenGui') then
    elseif ((v158.Name == 'reel') and v23) then
        local v508 = ReplicatedStorage:WaitForChild('events'):WaitForChild('reelfinished');
        if v508 then
            while v158 do
                local v619 = 0;
                while true do
                    if ((0) == v619) then
                        task.wait(2);
                        v508:FireServer(100, false);
                        break
                    end
                end
            end
        end
    end
end);
function Pidoras()
    spawn(function()
        while v24 do
            local v386 = game.Players.LocalPlayer;
            local v387 = v386.Character;
            if v387 then
                local v509 = 0;
                local v510;
                while true do
                    if (1 == v509) then
                        task.wait(1);
                        break
                    end
                    if ((0) == v509) then
                        v510 = v387:FindFirstChildOfClass('Tool');
                        if v510 then
                            local v735 = 0;
                            local v736;
                            while true do
                                if (v735 == (0)) then
                                    v736 = v510:FindFirstChild('bobber');
                                    if not v736 then
                                        local v824 = v510:FindFirstChild('events') and v510.events:FindFirstChild('cast') ;
                                        if v824 then
                                            local v849 = 0;
                                            local v850;
                                            local v851;
                                            local v852;
                                            local v853;
                                            while true do
                                                if (1 == v849) then
                                                    print(v851);
                                                    v852 = math.random(90, 99);
                                                    v849 = 2;
                                                end
                                                if (3 == v849) then
                                                    if v853 then
                                                        v853.Anchored = false;
                                                    end
                                                    break
                                                end
                                                if (v849 == (2)) then
                                                    v824:FireServer(v852);
                                                    v853 = v387:FindFirstChild('HumanoidRootPart');
                                                    v849 = 3;
                                                end
                                                if ((0) == v849) then
                                                    v850 = (math.random() * (9)) + (90) ;
                                                    v851 = string.format('%.4f', v850);
                                                    v849 = 1;
                                                end
                                            end
                                        end
                                    end
                                    break
                                end
                            end
                        end
                        v509 = 1;
                    end
                end
            end
        end
    end);
end
NoclipConnection = RunService.Stepped:Connect(function()
    if (v25 == true) then
        if (v12 ~= nil) then
            for v536, v537 in pairs(v12:GetDescendants()) do
                if (v537:IsA('BasePart') and (v537.CanCollide == true)) then
                    v537.CanCollide = false;
                end
            end
        end
    end
end);
local v32;
function rememberPosition()
    spawn(function()
        local v335 = game.Players.LocalPlayer;
        local v336 = v335.Character or v335.CharacterAdded:Wait() ;
        local v337 = v336:FindFirstChildOfClass('Humanoid');
        local v338 = v336:WaitForChild('HumanoidRootPart');
        local v339 = v338.CFrame;
        local v340 = Instance.new('BodyVelocity');
        v340.Velocity = Vector3.new(0, 0, 0);
        v340.MaxForce = Vector3.new(math.huge, math.huge, math.huge);
        v340.Parent = v338;
        local v344 = Instance.new('BodyGyro');
        v344.MaxTorque = Vector3.new(math.huge, math.huge, math.huge);
        v344.D = 100;
        v344.P = 10000;
        v344.CFrame = v339;
        v344.Parent = v338;
        while v16 do
            local v388 = 0;
            while true do
                if (v388 == (0)) then
                    v338.CFrame = v339;
                    task.wait(1E-2);
                    break
                end
            end
        end
        if v340 then
            v340:Destroy();
        end
        if v344 then
            v344:Destroy();
        end
    end);
end
local v33 = v10.Main:AddDropdown('DropdownShake', {
    Title = 'Select Auto Shake Mode:',
    Description = 'For the Mouse Method: Please ensure that the UI is hidden and the chat is toggled off to enable the auto-shake functionality.',
    Values = {
        'Mouse',
        'Phantom'
    },
    Multi = false,
    Default = 1
});
v33:OnChanged(function(v159)
    local v160 = 0;
    while true do
        if (v160 == (0)) then
            ShakeMode = v159;
            print('Auto Shake Mode:', v159);
            break
        end
    end
end);
local v34 = v10.Main:AddSlider('Slider', {
    Title = 'AutoShake Delay',
    Description = "",
    Default = 2,
    Min = 0.2,
    Max = 1,
    Rounding = 1,
    Callback = function(v161)
        v22 = v161;
    end
});
v34:OnChanged(function(v162)
    v22 = v162;
end);
v34:SetValue(0.5);
local v35 = v10.Main:AddToggle('autoReelCastShakeT', {
    Title = 'Auto Fish',
    Default = false
});
v35:OnChanged(function(v163)
    v23 = v163;
    v24 = v163;
    if v24 then
        Pidoras();
    end
    if (ShakeMode == 'Mouse') then
        v17 = v163;
    elseif (ShakeMode == 'Phantom') then
        v19 = v163;
    end
    v18 = v163;
    AutoFish5();
    if ((v24 == true) and (v12:FindFirstChildOfClass('Tool') ~= nil)) then
        local v389 = 0;
        local v390;
        while true do
            if (v389 == (0)) then
                v390 = v12:FindFirstChildOfClass('Tool');
                if (v390:FindFirstChild('events'):WaitForChild('cast') ~= nil) then
                    local v621 = 0;
                    local v622;
                    local v623;
                    local v624;
                    while true do
                        if (1 == v621) then
                            print(v623);
                            v624 = math.random(90, 99);
                            v621 = 2;
                        end
                        if (2 == v621) then
                            v390.events.cast:FireServer(v624);
                            break
                        end
                        if (v621 == 0) then
                            local v751 = 0;
                            while true do
                                if (0 == v751) then
                                    v622 = (math.random() * (9)) + (90) ;
                                    v623 = string.format('%.4f', v622);
                                    v751 = 1;
                                end
                                if (v751 == 1) then
                                    v621 = 1;
                                    break
                                end
                            end
                        end
                    end
                end
                break
            end
        end
    end
end);
local v36;
local v37 = false;
local v38 = v10.Main:AddParagraph({
    Title = 'Position :',
    Content = ""
});
v10.Main:AddButton({
    Title = 'Select Position',
    Description = "",
    Callback = function()
        local v164 = 0;
        local v165;
        local v166;
        local v167;
        while true do
            if (v164 == (1)) then
                v166 = v165.Character or v165.CharacterAdded:Wait() ;
                v167 = v166:FindFirstChild('HumanoidRootPart');
                v164 = 2;
            end
            if (v164 == (0)) then
                v165 = game.Players.LocalPlayer;
                if not v165 then
                    return
                end
                v164 = 1;
            end
            if (2 == v164) then
                if v167 then
                    local v539 = 0;
                    local v540;
                    while true do
                        if (v539 == (0)) then
                            v540 = v167.Position;
                            v36 = CFrame.new(v540) * v167.CFrame.Rotation ;
                            v539 = 1;
                        end
                        if (v539 == 1) then
                            v38:SetTitle('Position : ' .. tostring(math.floor(v540.X)) .. ' X ' .. tostring(math.floor(v540.Y)) .. ' Y ' .. tostring(math.floor(v540.Z)) .. ' Z');
                            break
                        end
                    end
                else
                    v38:SetTitle('Error: Unable to find player position.');
                end
                break
            end
        end
    end
});
v10.Main:AddToggle('MyToggle', {
    Title = 'Teleport to selected location',
    Description = "",
    Default = false,
    Callback = function(v168)
        if v168 then
            print('Toggle On');
            v37 = true;
            while v37 do
                local v425 = 0;
                local v426;
                while true do
                    if (v425 == (1)) then
                        task.wait();
                        break
                    end
                    if (v425 == (0)) then
                        local v590 = 0;
                        local v591;
                        while true do
                            if (v590 == (0)) then
                                v591 = 0;
                                while true do
                                    if (v591 == (0)) then
                                        v426 = game.Players.LocalPlayer;
                                        if (v426 and v36) then
                                            local v825 = v426.Character;
                                            if (v825 and v825:FindFirstChild('HumanoidRootPart')) then
                                                v825.HumanoidRootPart.CFrame = v36;
                                            end
                                        end
                                        v591 = 1;
                                    end
                                    if (v591 == 1) then
                                        v425 = 1;
                                        break
                                    end
                                end
                                break
                            end
                        end
                    end
                end
            end
        else
            local v391 = 0;
            while true do
                if (v391 == (0)) then
                    print('Toggle Off');
                    v37 = false;
                    break
                end
            end
        end
    end
});
v10.Main:AddButton({
    Title = 'Sell Holding Fish',
    Description = "",
    Callback = function()
        Workspace:WaitForChild('world'):WaitForChild('npcs'):WaitForChild('Marc Merchant'):WaitForChild('merchant'):WaitForChild('sell'):InvokeServer();
    end
});
v10.Main:AddButton({
    Title = 'Sell All Fishes',
    Description = "",
    Callback = function()
        Workspace:WaitForChild('world'):WaitForChild('npcs'):WaitForChild('Marc Merchant'):WaitForChild('merchant'):WaitForChild('sellall'):InvokeServer();
    end
});
v10.Main:AddButton({
    Title = 'Appraise fish',
    Description = "",
    Callback = function()
        Workspace:WaitForChild('world'):WaitForChild('npcs'):WaitForChild('Appraiser'):WaitForChild('appraiser'):WaitForChild('appraise'):InvokeServer();
    end
});
local v39 = v10.Main:AddToggle('MyToggle', {
    Title = 'Bypass Radar',
    Description = "",
    Default = false,
    Callback = function(v169)
        if v169 then
            for v427, v428 in pairs(game:GetService('CollectionService'):GetTagged('radarTag')) do
                if (v428:IsA('BillboardGui') or v428:IsA('SurfaceGui')) then
                    v428.Enabled = true;
                end
            end
        else
            for v429, v430 in pairs(game:GetService('CollectionService'):GetTagged('radarTag')) do
                if (v430:IsA('BillboardGui') or v430:IsA('SurfaceGui')) then
                    v430.Enabled = false;
                end
            end
        end
    end
});
local function v40()
    local v170 = 0;
    local v171;
    local v172;
    local v173;
    while true do
        if (v170 == (0)) then
            v171 = game.Players.LocalPlayer;
            v172 = v171.Character or v171.CharacterAdded:Wait() ;
            v170 = 1;
        end
        if (v170 == (1)) then
            v173 = v172:WaitForChild('HumanoidRootPart');
            if v173 then
                local v543 = 0;
                local v544;
                while true do
                    if (v543 == (0)) then
                        v544 = v173.Position;
                        return {
                            v544.X,
                            v544.Y,
                            v544.Z
                        }
                    end
                end
            else
                return {
                    0,
                    0,
                    0
                }
            end
            break
        end
    end
end
local function v41(v174)
    return string.format('%.1f', v174)
end
local v42;
local v39 = v10.Main:AddToggle('Bypass GPS', {
    Title = 'Bypass Gps',
    Description = "",
    Default = false,
    Callback = function(v175)
        if v175 then
            local v392 = game:GetService('ReplicatedStorage').resources.items.items.GPS.GPS.gpsMain.xyz:Clone();
            v392.Parent = game.Players.LocalPlayer.PlayerGui:WaitForChild('hud'):WaitForChild('safezone'):WaitForChild('backpack');
            local v394 = v40();
            local v395 = string.format('%s, %s, %s', v41(v394[1]), v41(v394[2]), v41(v394[3]));
            v392.Text = "<font color='#ff4949'>X</font><font color='#a3ff81'>Y</font><font color='#626aff'>Z</font>: " .. v395 ;
            v42 = game:GetService('RunService').Heartbeat:Connect(function()
                local v432 = 0;
                local v433;
                local v434;
                while true do
                    if (v432 == (0)) then
                        local v592 = 0;
                        while true do
                            if (v592 == (0)) then
                                v433 = v40();
                                v434 = string.format('%s, %s, %s', v41(v433[1]), v41(v433[2]), v41(v433[3]));
                                v592 = 1;
                            end
                            if (v592 == 1) then
                                v432 = 1;
                                break
                            end
                        end
                    end
                    if (v432 == (1)) then
                        v392.Text = "<font color='#ff4949'>X</font><font color='#a3ff81'>Y</font><font color='#626aff'>Z</font>: " .. v434 ;
                        break
                    end
                end
            end);
        else
            local v397 = 0;
            local v398;
            local v399;
            while true do
                if ((1) == v397) then
                    if v399:FindFirstChild('xyz') then
                        v399:FindFirstChild('xyz'):Destroy();
                    end
                    if v42 then
                        local v625 = 0;
                        while true do
                            if (v625 == (0)) then
                                v42:Disconnect();
                                v42 = nil;
                                break
                            end
                        end
                    end
                    break
                end
                if (v397 == (0)) then
                    v398 = game.Players.LocalPlayer:WaitForChild('PlayerGui');
                    v399 = v398:WaitForChild('hud'):WaitForChild('safezone'):WaitForChild('backpack');
                    v397 = 1;
                end
            end
        end
    end
});
local v43 = false;
local v39 = v10.Main:AddToggle('MyToggle', {
    Title = 'AntiCheat',
    Description = "",
    Default = false,
    Callback = function(v176)
        if (v176 ~= v43) then
            local v400 = 0;
            while true do
                if (v400 == (0)) then
                    if v176 then
                        v8:Notify({
                            Title = 'Anti Cheat Enable',
                            Content = "Now Do Whatever You Want You're Immortal",
                            Duration = 5
                        });
                    else
                        v8:Notify({
                            Title = 'Anti Cheat Disable',
                            Content = 'Chance of getting ban increased by 43%',
                            Duration = 5
                        });
                    end
                    v43 = v176;
                    break
                end
            end
        end
    end
});
v10.Main:AddButton({
    Title = 'AutoReel + AutoShake + AutoCast',
    Description = 'Old One',
    Callback = function()
        local v177 = loadstring(game:HttpGet('https://raw.githubusercontent.com/Turtle-Brand/Turtle-Lib/main/source.lua'))();
        local v178 = v177:Window('NEOX HUB', {
            Color = Color3.fromRGB(25, 35, 45),
            Size = UDim2.new(0, 500, 0, 400)
        });
        local v179 = game:GetService('Players');
        local v180 = game:GetService('StarterGui');
        local v181 = game:GetService('GuiService');
        local v182 = game:GetService('ReplicatedStorage');
        local v183 = game:GetService('ContextActionService');
        local v184 = game:GetService('VirtualInputManager');
        local v185 = game:GetService('UserInputService');
        local v186 = v179.LocalPlayer;
        local v187 = false;
        local v188;
        local v189 = false;
        local v190 = false;
        local v191;
        local v192 = Enum.KeyCode.X;
        local v193 = 0;
        local function v194(v350, v351)
            v180:SetCore('SendNotification', {
                Title = 'NEOX HUB',
                Text = v350,
                Duration = v351 or (0.5),
                Button1Text = 'Okay'
            });
        end
        local function v195(v352, v353)
            if (v353 == Enum.UserInputState.Begin) then
                local v435 = 0;
                while true do
                    if (v435 == (0)) then
                        v187 = not v187;
                        if v187 then
                            v191 = v186.Character.HumanoidRootPart.Position;
                            farmStartTime = tick();
                            v194('Auto Farm: Enabled', 1.5);
                        else
                            local v673 = 0;
                            while true do
                                if (v673 == 2) then
                                    v194('Auto Farm: Disabled', 1.5);
                                    break
                                end
                                if (v673 == (0)) then
                                    v190 = false;
                                    v189 = false;
                                    v673 = 1;
                                end
                                if (v673 == (1)) then
                                    v181.SelectedObject = nil;
                                    if v188 then
                                        v188.events.reset:FireServer();
                                    end
                                    v673 = 2;
                                end
                            end
                        end
                        break
                    end
                end
            end
        end
        v186.Character.ChildAdded:Connect(function(v354)
            if (v354:IsA('Tool') and v354.Name:lower():find('rod')) then
                v188 = v354;
            end
        end);
        v186.Character.ChildRemoved:Connect(function(v355)
            if (v355 == v188) then
                v187 = false;
                v190 = false;
                v189 = false;
                v188 = nil;
                v181.SelectedObject = nil;
            end
        end);
        v186.PlayerGui.DescendantAdded:Connect(function(v356)
            if v187 then
                if ((v356.Name == 'button') and (v356.Parent.Name == 'safezone')) then
                    local v545 = 0;
                    while true do
                        if (v545 == (2)) then
                            task.wait(0.3);
                            v181.SelectedObject = nil;
                            break
                        end
                        if (v545 == (0)) then
                            task.wait(0.3);
                            v181.SelectedObject = v356;
                            v545 = 1;
                        end
                        if (v545 == (1)) then
                            v184:SendKeyEvent(true, Enum.KeyCode.Return, false, game);
                            v184:SendKeyEvent(false, Enum.KeyCode.Return, false, game);
                            v545 = 2;
                        end
                    end
                elseif ((v356.Name == 'playerbar') and (v356.Parent.Name == 'bar')) then
                    v190 = true;
                    v356:GetPropertyChangedSignal('Position'):Wait();
                    v182.events.reelfinished:FireServer(100, true);
                    v193 = v193 + (1) ;
                end
            end
        end);
        v186.PlayerGui.DescendantRemoving:Connect(function(v357)
            if (v357.Name == 'reel') then
                local v437 = 0;
                while true do
                    if (v437 == 0) then
                        v190 = false;
                        v189 = false;
                        break
                    end
                end
            end
        end);
        task.spawn(function()
            while true do
                if (v187 and not v189) then
                    if v188 then
                        local v594 = 0;
                        while true do
                            if (v594 == 0) then
                                v189 = true;
                                task.wait(0.5);
                                v594 = 1;
                            end
                            if (v594 == 1) then
                                v188.events.reset:FireServer();
                                v188.events.cast:FireServer(100.5);
                                break
                            end
                        end
                    end
                end
                task.wait();
            end
        end);
        task.spawn(function()
            while true do
                if v187 then
                    v186.Character.HumanoidRootPart.Position = v191;
                end
                task.wait(0.75);
            end
        end);
        if not v185.KeyboardEnabled then
            local v401 = 0;
            while true do
                if (0 == v401) then
                    v183:BindAction('ToggleFarm', v195, false, v192, Enum.UserInputType.Touch);
                    v183:SetTitle('ToggleFarm', 'Toggle Farm');
                    v401 = 1;
                end
                if (v401 == (1)) then
                    v183:SetPosition('ToggleFarm', UDim2.new(0.9, - 50, 0.8999999999999773, - 150));
                    v194('Press the onscreen button to enable/disable', 3);
                    break
                end
            end
        else
            v183:BindAction('ToggleFarm', v195, false, v192);
            v194(string.format('NEOX HUB', v192.Name), 3);
        end
        local v196 = v178:Label('Auto Farm Status: OFF', Color3.fromRGB(255, 165, 0));
        local v197 = v178:Label('Catches: 0', Color3.fromRGB(127, 143, 166));
        task.spawn(function()
            while true do
                local v402 = 0;
                while true do
                    if (v402 == (1)) then
                        task.wait(1);
                        break
                    end
                    if ((0) == v402) then
                        if v187 then
                            v196.Text = 'Auto Farm Status: ON';
                        else
                            v196.Text = 'Auto Farm Status: OFF';
                        end
                        v197.Text = 'Fishes Catches: ' .. v193 ;
                        v402 = 1;
                    end
                end
            end
        end);
        v178:Label('BETTER VERSION WITHOUT BUGS', Color3.fromRGB(255, 0, 0));
        v178:Label('How To Enable : X - ON/OFF', Color3.fromRGB(255, 165, 0));
    end
});
local v39 = v10.Misc:AddToggle('MyToggle', {
    Title = 'Freeze Character',
    Description = "",
    Default = false,
    Callback = function(v198)
        local v199 = game:GetService('Players').LocalPlayer;
        if (v199 and v199.Character and v199.Character:FindFirstChild('HumanoidRootPart')) then
            if v198 then
                v199.Character.HumanoidRootPart.Anchored = true;
                print('bro saw baddie and bro got Shocked.');
            else
                local v513 = 0;
                while true do
                    if (v513 == 0) then
                        v199.Character.HumanoidRootPart.Anchored = false;
                        print('bro saw ugly ass and start moving.');
                        break
                    end
                end
            end
        else
            warn('Player or HumanoidRootPart not found!');
        end
    end
});
v10.Misc:AddButton({
    Title = 'Anti AFK',
    Description = "",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/hassanxzayn-lua/Anti-afk/main/antiafkbyhassanxzyn'))();
    end
});
local v44 = v10.Misc:AddToggle('UnlimitedOxygenToggle', {
    Title = 'Unlimited Oxygen',
    Description = "",
    Default = false,
    Callback = function(v200)
        local v201 = 0;
        local v202;
        local v203;
        while true do
            if (0 == v201) then
                v202 = game.Players.LocalPlayer;
                v203 = v202.Character or v202.CharacterAdded:Wait() ;
                v201 = 1;
            end
            if (v201 == 1) then
                if v200 then
                    local v547 = 0;
                    while true do
                        if (v547 == 0) then
                            if (v203 and v203:FindFirstChild('client') and v203.client:FindFirstChild('oxygen')) then
                                local v752 = 0;
                                local v753;
                                while true do
                                    if (v752 == (0)) then
                                        v753 = v203.client.oxygen;
                                        if (v753 and v753.Enabled) then
                                            local v840 = 0;
                                            local v841;
                                            while true do
                                                if (v840 == 0) then
                                                    v841 = 0;
                                                    while true do
                                                        if (v841 == (0)) then
                                                            v753.Enabled = false;
                                                            print('Bro Is Immortal ahhh');
                                                            break
                                                        end
                                                    end
                                                    break
                                                end
                                            end
                                        end
                                        break
                                    end
                                end
                            end
                            v202.CharacterAdded:Connect(function()
                                local v737 = 0;
                                while true do
                                    if (v737 == (0)) then
                                        v203 = v202.Character or v202.CharacterAdded:Wait() ;
                                        if (v203 and v203:FindFirstChild('client') and v203.client:FindFirstChild('oxygen')) then
                                            local v826 = 0;
                                            local v827;
                                            while true do
                                                if (v826 == (0)) then
                                                    v827 = v203.client.oxygen;
                                                    if (v827 and v827.Enabled) then
                                                        v827.Enabled = false;
                                                    end
                                                    break
                                                end
                                            end
                                        end
                                        break
                                    end
                                end
                            end);
                            break
                        end
                    end
                elseif (v203 and v203:FindFirstChild('client') and v203.client:FindFirstChild('oxygen')) then
                    local v629 = 0;
                    local v630;
                    while true do
                        if (v629 == (0)) then
                            v630 = v203.client.oxygen;
                            if (v630 and not v630.Enabled) then
                                local v796 = 0;
                                while true do
                                    if (v796 == (0)) then
                                        v630.Enabled = true;
                                        print('Oxygen is now enabled.');
                                        break
                                    end
                                end
                            end
                            break
                        end
                    end
                end
                break
            end
        end
    end
});
local v44 = v10.Misc:AddToggle('UnlimitedOxygenToggle', {
    Title = 'Unlimited Oxygen (peaks)',
    Description = "",
    Default = false,
    Callback = function(v204)
        local v205 = game.Players.LocalPlayer;
        local v206 = v205.Character or v205.CharacterAdded:Wait() ;
        if v204 then
            local v403 = 0;
            while true do
                if (v403 == 0) then
                    if (v206 and v206:FindFirstChild('client') and v206.client:FindFirstChild('oxygen(peaks)')) then
                        local v631 = 0;
                        local v632;
                        while true do
                            if (v631 == (0)) then
                                v632 = v206.client['oxygen(peaks)'];
                                if (v632 and v632.Enabled) then
                                    local v797 = 0;
                                    local v798;
                                    while true do
                                        if (v797 == (0)) then
                                            v798 = 0;
                                            while true do
                                                if (v798 == (0)) then
                                                    v632.Enabled = false;
                                                    print('Bro Is Immortal ahhh');
                                                    break
                                                end
                                            end
                                            break
                                        end
                                    end
                                end
                                break
                            end
                        end
                    end
                    v205.CharacterAdded:Connect(function()
                        v206 = v205.Character or v205.CharacterAdded:Wait() ;
                        if (v206 and v206:FindFirstChild('client') and v206.client:FindFirstChild('oxygen(peaks)')) then
                            local v676 = 0;
                            local v677;
                            while true do
                                if (v676 == (0)) then
                                    v677 = v206.client['oxygen(peaks)'];
                                    if (v677 and v677.Enabled) then
                                        v677.Enabled = false;
                                    end
                                    break
                                end
                            end
                        end
                    end);
                    break
                end
            end
        elseif (v206 and v206:FindFirstChild('client') and v206.client:FindFirstChild('oxygen(peaks)')) then
            local v514 = v206.client['oxygen(peaks)'];
            if (v514 and not v514.Enabled) then
                v514.Enabled = true;
                print('Oxygen(peaks) is now enabled.');
            end
        end
    end
});
local v45 = v10.Misc:AddToggle('UnlimitedTempToggle', {
    Title = 'Unlimited Temprature',
    Description = "",
    Default = false,
    Callback = function(v207)
        local v208 = game.Players.LocalPlayer;
        local v209 = v208.Character or v208.CharacterAdded:Wait() ;
        if v207 then
            if (v209 and v209:FindFirstChild('client') and v209.client:FindFirstChild('temperature')) then
                local v515 = 0;
                local v516;
                while true do
                    if (v515 == (0)) then
                        v516 = v209.client.temperature;
                        if (v516 and v516.Enabled) then
                            v516.Enabled = false;
                            print('Bro Is Immortal ahhh');
                        end
                        break
                    end
                end
            end
            v208.CharacterAdded:Connect(function()
                local v439 = 0;
                while true do
                    if ((0) == v439) then
                        v209 = v208.Character or v208.CharacterAdded:Wait() ;
                        if (v209 and v209:FindFirstChild('client') and v209.client:FindFirstChild('temperature')) then
                            local v678 = 0;
                            local v679;
                            while true do
                                if (v678 == (0)) then
                                    v679 = v209.client.temperature;
                                    if (v679 and v679.Enabled) then
                                        v679.Enabled = false;
                                    end
                                    break
                                end
                            end
                        end
                        break
                    end
                end
            end);
        elseif (v209 and v209:FindFirstChild('client') and v209.client:FindFirstChild('temperature')) then
            local v517 = v209.client.temperature;
            if (v517 and not v517.Enabled) then
                v517.Enabled = true;
                print('temperature is now enabled.');
            end
        end
    end
});
local v46 = v10.Misc:AddToggle('Walk On Water', {
    Title = 'Walk On Water',
    Description = "",
    Default = false,
    Callback = function(v210)
        for v358, v359 in pairs(workspace.zones.fishing:GetChildren()) do
            if (v359.Name == 'Ocean') then
                v359.CanCollide = v210;
            end
        end
    end
});
local v47 = v10.Misc:AddDropdown('WalkOnWaterZone', {
    Title = 'Walk On Water Zone',
    Values = {
        'Ocean',
        'Desolate Deep',
        'The Depths'
    },
    Multi = false,
    Default = 'Ocean'
});
v47:OnChanged(function(v211)
    WalkZone = v211;
end);
local v48 = v10.Misc:AddToggle('DisableSwimmingToggle', {
    Title = 'Disable Swimming',
    Description = "",
    Default = false,
    Callback = function(v212)
        local v213 = 0;
        local v214;
        local v215;
        while true do
            if (v213 == (0)) then
                local v441 = 0;
                while true do
                    if (v441 == (1)) then
                        v213 = 1;
                        break
                    end
                    if (v441 == (0)) then
                        v214 = game.Players.LocalPlayer;
                        v215 = v214.Character or v214.CharacterAdded:Wait() ;
                        v441 = 1;
                    end
                end
            end
            if (v213 == (1)) then
                if (v215 and v215:FindFirstChild('Humanoid')) then
                    local v548 = 0;
                    local v549;
                    while true do
                        if (v548 == 0) then
                            v549 = v215:FindFirstChild('Humanoid');
                            if v549 then
                                if v212 then
                                    v549:SetStateEnabled(Enum.HumanoidStateType.Swimming, false);
                                    print('bro why you stop swimming');
                                else
                                    local v799 = 0;
                                    while true do
                                        if (v799 == (0)) then
                                            v549:SetStateEnabled(Enum.HumanoidStateType.Swimming, true);
                                            print('bro start swimming');
                                            break
                                        end
                                    end
                                end
                            end
                            break
                        end
                    end
                else
                    warn('Humanoid not found!');
                end
                break
            end
        end
    end
});
local v49 = game.Players.LocalPlayer:WaitForChild('PlayerGui');
local v50 = v10.Misc:AddToggle('JustUI', {
    Title = 'Show/Hide UIs',
    Default = true
});
v50:OnChanged(function()
    local v216 = 0;
    local v217;
    while true do
        if (v216 == 0) then
            v217 = v50.Value;
            if (v49:FindFirstChild('hud') and v49.hud:FindFirstChild('safezone')) then
                v49.hud.safezone.Visible = v217;
            else
                warn('hud or safezone not found in PlayerGui');
            end
            break
        end
    end
end);
v10.Misc:AddButton({
    Title = 'Remove AFK Tag',
    Description = "",
    Callback = function()
        local v218 = 0;
        local v219;
        local v220;
        while true do
            if (v218 == (1)) then
                if v220 then
                    v220:Destroy();
                    print('AFK event removed.');
                else
                    print('AFK event not found.');
                end
                break
            end
            if (v218 == (0)) then
                v219 = game:GetService('ReplicatedStorage');
                v220 = v219:FindFirstChild('events') and v219.events:FindFirstChild('afk') ;
                v218 = 1;
            end
        end
    end
});
local v51 = Instance.new('ScreenGui');
v51.Name = 'BlackGui';
v51.ResetOnSpawn = false;
local v54 = Instance.new('Frame');
v54.Name = 'BlackFrame';
v54.Size = UDim2.new(1, 0, 1, 0);
v54.BackgroundColor3 = Color3.new(0, 0, 0);
v54.BackgroundTransparency = 1;
v54.Parent = v51;
v51.Parent = game.Players.LocalPlayer:WaitForChild('PlayerGui');
local v61 = Instance.new('ScreenGui');
v61.Name = 'WhiteGui';
v61.ResetOnSpawn = false;
local v64 = Instance.new('Frame');
v64.Name = 'WhiteFrame';
v64.Size = UDim2.new(1, 0, 1, 0);
v64.BackgroundColor3 = Color3.new(1, 1, 1);
v64.BackgroundTransparency = 1;
v64.Parent = v61;
v61.Parent = game.Players.LocalPlayer:WaitForChild('PlayerGui');
local v71 = v10.Misc:AddToggle('BlackGui5', {
    Title = 'Black Screen',
    Default = false
});
v71:OnChanged(function()
    local v221 = 0;
    local v222;
    while true do
        if (v221 == (0)) then
            v222 = v71.Value;
            if v222 then
                v54.BackgroundTransparency = 0;
            else
                v54.BackgroundTransparency = 1;
            end
            break
        end
    end
end);
local v72 = v10.Misc:AddToggle('WhiteGui5', {
    Title = 'White Screen',
    Default = false
});
v72:OnChanged(function()
    local v223 = 0;
    local v224;
    while true do
        if (v223 == 0) then
            v224 = v72.Value;
            if v224 then
                v64.BackgroundTransparency = 0;
            else
                v64.BackgroundTransparency = 1;
            end
            break
        end
    end
end);
v10.Misc:AddButton({
    Title = 'Infiniteyield Reborn',
    Description = "",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/RyXeleron/infiniteyield-reborn/refs/heads/scriptblox/source'))();
    end
});
local v39 = v10.Misc:AddToggle('MyToggle', {
    Title = 'Hide Leaderstats',
    Description = "",
    Default = false,
    Callback = function(v225)
        local v226 = game.Players.LocalPlayer;
        local v227 = v226:FindFirstChild('leaderstats');
        if v227 then
            local v404 = 0;
            local v405;
            local v406;
            while true do
                if (v404 == 0) then
                    v405 = v227:FindFirstChild('C$');
                    v406 = v227:FindFirstChild('Level');
                    v404 = 1;
                end
                if ((1) == v404) then
                    if v225 then
                        local v634 = 0;
                        while true do
                            if (v634 == 0) then
                                if (v405 and v405:IsA('StringValue')) then
                                    local v800 = 0;
                                    while true do
                                        if (v800 == (0)) then
                                            v405:SetAttribute('OriginalValue', v405.Value);
                                            v405.Value = 'Hidden';
                                            break
                                        end
                                    end
                                end
                                if (v406 and v406:IsA('NumberValue')) then
                                    v406:SetAttribute('OriginalValue', v406.Value);
                                    v406.Value = 0;
                                end
                                break
                            end
                        end
                    else
                        local v635 = 0;
                        while true do
                            if (v635 == (0)) then
                                if (v405 and v405:IsA('StringValue')) then
                                    local v802 = v405:GetAttribute('OriginalValue');
                                    if v802 then
                                        v405.Value = v802;
                                    end
                                end
                                if (v406 and v406:IsA('NumberValue')) then
                                    local v803 = 0;
                                    local v804;
                                    while true do
                                        if (v803 == 0) then
                                            v804 = v406:GetAttribute('OriginalValue');
                                            if v804 then
                                                v406.Value = v804;
                                            end
                                            break
                                        end
                                    end
                                end
                                break
                            end
                        end
                    end
                    break
                end
            end
        else
            warn('Leaderstats not found!');
        end
    end
});
local v73 = v10.Misc:AddSection('Character');
local v74 = v10.Misc:AddToggle('TeleportToggle', {
    Title = 'T + Left Click Teleport',
    Description = "",
    Default = false,
    Callback = function(v228)
        local v229 = 0;
        while true do
            if (v229 == 1) then
                if v228 then
                    if not connection then
                        connection = game:GetService('UserInputService').InputBegan:Connect(function(v680, v681)
                            if (not v681 and isTeleportEnabled and (v680.UserInputType == Enum.UserInputType.MouseButton1)) then
                                if game:GetService('UserInputService'):IsKeyDown(Enum.KeyCode.T) then
                                    local v805 = 0;
                                    local v806;
                                    local v807;
                                    local v808;
                                    while true do
                                        if (v805 == 1) then
                                            v808 = nil;
                                            while true do
                                                if (v806 == (1)) then
                                                    v807.Character:MoveTo(Vector3.new(v808.Hit.x, v808.Hit.y, v808.Hit.z));
                                                    break
                                                end
                                                if ((0) == v806) then
                                                    v807 = game:GetService('Players').LocalPlayer;
                                                    v808 = v807:GetMouse();
                                                    v806 = 1;
                                                end
                                            end
                                            break
                                        end
                                        if (v805 == (0)) then
                                            v806 = 0;
                                            v807 = nil;
                                            v805 = 1;
                                        end
                                    end
                                end
                            end
                        end);
                    end
                elseif connection then
                    local v636 = 0;
                    local v637;
                    while true do
                        if (v636 == (0)) then
                            v637 = 0;
                            while true do
                                if (v637 == (0)) then
                                    connection:Disconnect();
                                    connection = nil;
                                    break
                                end
                            end
                            break
                        end
                    end
                end
                break
            end
            if (v229 == 0) then
                if (not hasUserToggled and not isTeleportEnabled) then
                    hasUserToggled = true;
                    isTeleportEnabled = v228;
                    return
                end
                isTeleportEnabled = v228;
                v229 = 1;
            end
        end
    end
});
local v75 = v10.Misc:AddToggle('InfiniteJumpToggle', {
    Title = 'Infinite Jumps',
    Description = "",
    Default = false,
    Callback = function(v230)
        _G.infinjump = v230;
    end
});
if not _G.infinJumpStarted then
    local v360 = 0;
    local v361;
    local v362;
    while true do
        if (v360 == (2)) then
            v362.KeyDown:Connect(function(v555)
                if _G.infinjump then
                    if (v555:byte() == (32)) then
                        local v739 = 0;
                        local v740;
                        while true do
                            if (v739 == (0)) then
                                v740 = v361.Character and v361.Character:FindFirstChildOfClass('Humanoid') ;
                                if v740 then
                                    local v829 = 0;
                                    while true do
                                        if (v829 == 1) then
                                            v740:ChangeState('Seated');
                                            break
                                        end
                                        if (v829 == (0)) then
                                            v740:ChangeState('Jumping');
                                            wait();
                                            v829 = 1;
                                        end
                                    end
                                end
                                break
                            end
                        end
                    end
                end
            end);
            break
        end
        if (v360 == 0) then
            _G.infinJumpStarted = true;
            _G.infinjump = false;
            v360 = 1;
        end
        if (v360 == 1) then
            local v518 = 0;
            while true do
                if (v518 == (1)) then
                    v360 = 2;
                    break
                end
                if (v518 == (0)) then
                    v361 = game:GetService('Players').LocalPlayer;
                    v362 = v361:GetMouse();
                    v518 = 1;
                end
            end
        end
    end
end
local v25;
local v76 = true;
function noclip()
    local v231 = 0;
    local v232;
    while true do
        if (v231 == (0)) then
            v76 = false;
            v232 = nil;
            v231 = 1;
        end
        if (v231 == (1)) then
            function v232()
                local v519 = 0;
                while true do
                    if (v519 == (0)) then
                        if ((v76 == false) and (game.Players.LocalPlayer.Character ~= nil)) then
                            for v756, v757 in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                                if (v757:IsA('BasePart') and v757.CanCollide and (v757.Name ~= floatName)) then
                                    v757.CanCollide = false;
                                end
                            end
                        end
                        wait(0.21);
                        break
                    end
                end
            end
            v25 = game:GetService('RunService').Stepped:Connect(v232);
            break
        end
    end
end
function clip()
    local v233 = 0;
    while true do
        if (v233 == (0)) then
            if v25 then
                v25:Disconnect();
            end
            v76 = true;
            v233 = 1;
        end
        if (v233 == 1) then
            if game.Players.LocalPlayer.Character then
                for v598, v599 in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                    if (v599:IsA('BasePart') and (v599.CanCollide == false)) then
                        v599.CanCollide = true;
                    end
                end
            end
            break
        end
    end
end
local v39 = v10.Misc:AddToggle('MyToggle', {
    Title = 'Noclip',
    Description = "",
    Default = false,
    Callback = function(v234)
        if v234 then
            noclip();
        else
            clip();
        end
    end
});
local v34 = v10.Misc:AddSlider('SpeedSlider', {
    Title = 'WalkSpeed',
    Description = "",
    Default = 16,
    Min = 16,
    Max = 500,
    Rounding = 1,
    Callback = function(v235)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v235;
    end
});
local v34 = v10.Misc:AddSlider('JumpSlider', {
    Title = 'Jump Power',
    Description = "",
    Default = 50,
    Min = 50,
    Max = 500,
    Rounding = 1,
    Callback = function(v237)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = v237;
    end
});
local v77 = game:GetService('RunService');
local v78;
local v34 = v10.Misc:AddSlider('GravitySlider', {
    Title = 'Gravity',
    Description = "",
    Default = 196,
    Min = 0,
    Max = 500,
    Rounding = 1,
    Callback = function(v239)
        local v240 = 0;
        while true do
            if (v240 == 1) then
                v78 = v77.RenderStepped:Connect(function()
                    workspace.Gravity = v239;
                end);
                break
            end
            if (v240 == (0)) then
                print('Gravity slider changed to:', v239);
                if v78 then
                    v78:Disconnect();
                end
                v240 = 1;
            end
        end
    end
});
local v34 = v10.Misc:AddSlider('AssSlider', {
    Title = 'HipHeight',
    Description = "",
    Default = 0,
    Min = 0,
    Max = 500,
    Rounding = 1,
    Callback = function(v241)
        game.Players.LocalPlayer.Character.Humanoid.HipHeight = v241;
    end
});
local v79 = v10.Misc:AddInput('FOVInput', {
    Title = 'Change FOV',
    Description = "",
    Default = '70',
    Placeholder = 'Enter FOV value',
    Numeric = true,
    Finished = true,
    Callback = function(v243)
        local v244 = tonumber(v243);
        if v244 then
            local v407 = 0;
            while true do
                if (0 == v407) then
                    game.Workspace.Camera.FieldOfView = v244;
                    print('FOV set to:', v244);
                    break
                end
            end
        else
            warn('Invalid FOV value entered');
        end
    end
});
local v80 = game:GetService('RunService');
local v81;
local v82 = v10.Weather:AddToggle('Only Day', {
    Title = 'Only Day',
    Description = "",
    Default = false,
    Callback = function(v245)
        if v245 then
            v81 = v80.Heartbeat:Connect(function()
                game:GetService('Lighting').TimeOfDay = '12:00:00';
            end);
        elseif v81 then
            local v521 = 0;
            while true do
                if (v521 == 0) then
                    v81:Disconnect();
                    v81 = nil;
                    break
                end
            end
        end
    end
});
local v83;
local v84 = v10.Weather:AddToggle('Only Night', {
    Title = 'Only Night',
    Description = "",
    Default = false,
    Callback = function(v246)
        if v246 then
            v83 = v80.Heartbeat:Connect(function()
                game:GetService('Lighting').TimeOfDay = '22:00:00';
            end);
        elseif v83 then
            local v522 = 0;
            while true do
                if (v522 == (0)) then
                    v83:Disconnect();
                    v83 = nil;
                    break
                end
            end
        end
    end
});
local v85 = v10.Weather:AddToggle('Remove Fog', {
    Title = 'Remove Fog',
    Description = "",
    Default = false,
    Callback = function(v247)
        if v247 then
            local v408 = game:GetService('Lighting'):FindFirstChild('Sky');
            if v408 then
                v408.Parent = game:GetService('Lighting').bloom;
            end
        else
            local v409 = 0;
            local v410;
            while true do
                if ((0) == v409) then
                    v410 = game:GetService('Lighting').bloom:FindFirstChild('Sky');
                    if v410 then
                        v410.Parent = game:GetService('Lighting');
                    end
                    break
                end
            end
        end
    end
});
local v86 = game:GetService('ReplicatedStorage');
local v87 = v10.Weather:AddToggle('Clear Weather', {
    Title = 'Clear Weather',
    Description = "",
    Default = false,
    Callback = function(v248)
        local v249 = v86:WaitForChild('world'):WaitForChild('weather').Value;
        if v248 then
            v86.world.weather.Value = 'Clear';
        else
            v86.world.weather.Value = v249;
        end
    end
});
v10.Teleport:AddButton({
    Title = 'Create Safe Zone',
    Callback = function()
        local v250 = 0;
        local v251;
        local v252;
        local v253;
        local v254;
        local v255;
        local v256;
        local v257;
        while true do
            if (v250 == (1)) then
                v254.Position = Vector3.new(math.random(- 2E3, 2000), math.random(50000, 90000), math.random(- 2E3, 2E3));
                v254.Anchored = true;
                v254.BrickColor = BrickColor.new('White');
                v254.TopSurface = Enum.SurfaceType.Studs;
                v254.Material = Enum.Material.Plastic;
                v254.Transparency = 0.2;
                v250 = 2;
            end
            if (v250 == 0) then
                v251 = game.Players.LocalPlayer;
                v252 = v251.Character or v251.CharacterAdded:Wait() ;
                v253 = v252:FindFirstChild('HumanoidRootPart');
                if not v253 then
                    local v557 = 0;
                    while true do
                        if (v557 == (0)) then
                            local v683 = 0;
                            while true do
                                if (v683 == 0) then
                                    warn('HumanoidRootPart not found!');
                                    return
                                end
                            end
                        end
                    end
                end
                v254 = Instance.new('Part');
                v254.Size = Vector3.new(30, 1, 30);
                v250 = 1;
            end
            if (v250 == (3)) then
                v256.Size = UDim2.new(1, 0, 0.5, 0);
                v256.Position = UDim2.new(0, 0, 0, 0);
                v256.BackgroundTransparency = 1;
                v256.Text = 'NEOX HUB';
                v256.TextColor3 = Color3.new(1, 0, 0);
                v256.TextScaled = true;
                v250 = 4;
            end
            if (v250 == (2)) then
                v254.Parent = game.Workspace;
                v255 = Instance.new('SurfaceGui');
                v255.Face = Enum.NormalId.Top;
                v255.Adornee = v254;
                v255.Parent = v254;
                v256 = Instance.new('TextLabel');
                v250 = 3;
            end
            if ((4) == v250) then
                v256.Font = Enum.Font.SourceSansBold;
                v256.Parent = v255;
                v257 = Instance.new('TextLabel');
                v257.Size = UDim2.new(1, 0, 0.5, 0);
                v257.Position = UDim2.new(0, 0, 0.5, 0);
                v257.BackgroundTransparency = 1;
                v250 = 5;
            end
            if ((5) == v250) then
                v257.Text = 'Join our Discord';
                v257.TextColor3 = Color3.new(0, 0, 1);
                v257.TextScaled = true;
                v257.Font = Enum.Font.SourceSansBold;
                v257.Parent = v255;
                v253.CFrame = v254.CFrame + Vector3.new(0, 5, 0) ;
                break
            end
        end
    end
});
local v88 = v10.Teleport:AddDropdown('TeleportLocationsDropdown', {
    Title = 'Teleport To Locations',
    Description = "",
    Values = {
        'Workshop',
        'Santa',
        'Merlin',
        'Forsaken',
        'Crafting',
        'Camp1',
        'Camp2',
        'Ancient Isle',
        'Ancientarchives',
        'North Glider',
        '???',
        'Final Puzzle',
        'The Depth Maze Exit',
        'Lever Puzzle',
        'The Depth Lobby',
        'Deep Shop',
        'Ice Puzzle',
        'Archive',
        'Desolate',
        'Mountain Start',
        'Elf',
        'Altar',
        'arch',
        'The_Depth',
        'birch',
        'Archeological Site',
        'brine',
        'deep',
        'enchant',
        'executive',
        'keepers',
        'mod_house',
        'moosewood',
        'mushgrove',
        'roslit',
        'snow',
        'snowcap',
        'spike',
        'statue',
        'sunstone',
        'swamp',
        'terrapin',
        'trident',
        'vertigo',
        'volcano',
        'wilson',
        'wilsons_rod'
    },
    Multi = false,
    Default = 'None',
    Callback = function(v258)
        local v259 = {
            Workshop = Vector3.new(- 156.24490356445313, 364.8857727050781, - 9462.23828125),
            Merlin = Vector3.new(- 949.0145874023438, 222.05545043945313, - 985.9754028320313),
            Ancientarchives = Vector3.new(- 3155.022216796875, - 754.818115234375, 2193.136962890625),
            Forsaken = Vector3.new(- 2498.24609375, 136.9497528076172, 1624.852294921875),
            Crafting = Vector3.new(- 3159.9951171875, - 745.614013671875, 1684.16796875),
            Camp1 = Vector3.new(20208.041015625, 208.42010498046875, 5278.67578125),
            Camp2 = Vector3.new(19756.58984375, 415.43707275390625, 5406.69970703125),
            ['Ancient Isle'] = Vector3.new(5948.79052734375, 154.9259033203125, 482.23583984375),
            ['North Glider'] = Vector3.new(20240.86328125, 756.5258178710938, 5756.46630859375),
            Santa = Vector3.new(- 142.2449951171875, 364.6358337402344, - 9498.23828125),
            ['???'] = Vector3.new(- 1479.493896484375, - 225.71063232421875, - 2391.423095703125),
            ['Final Puzzle'] = Vector3.new(19963.97265625, 1137.889404296875, 5401.83544921875),
            ['The Depth Maze Exit'] = Vector3.new(978.142822265625, - 701.1101684570313, 1253.7423095703125),
            ['Lever Puzzle'] = Vector3.new(19955.671875, 586.853759765625, 5571.53564453125),
            ['The Depth Lobby'] = Vector3.new(66.99270629882813, - 704.9685668945313, 1230.847900390625),
            ['Deep Shop'] = Vector3.new(- 979.1976318359375, - 244.91102600097656, - 2699.8740234375),
            ['Ice Puzzle'] = Vector3.new(19232.732421875, 395.87213134765625, 6010.345703125),
            Archive = Vector3.new(- 3157.536865234375, - 754.8175659179688, 2214.496826171875),
            Desolate = Vector3.new(- 1654.96728515625, - 213.67941284179688, - 2845.9521484375),
            ['Mountain Start'] = Vector3.new(19558.537109375, 132.67010498046875, 5301.47802734375),
            Elf = Vector3.new(- 10.68837833404541, 322.271728515625, - 9288.181640625),
            Altar = Vector3.new(1296.320068359375, - 808.5519409179688, - 298.93817138671875),
            The_Depth = Vector3.new(568.1527099609375, - 704.4259643554688, 1230.847900390625),
            ['Archeological Site'] = Vector3.new(4050, 130, 50),
            arch = Vector3.new(998.966796875, 126.6849365234375, - 1237.1434326171875),
            birch = Vector3.new(1742.3203125, 138.25787353515625, - 2502.23779296875),
            brine = Vector3.new(- 1794.1134033203125, - 142.86239624023438, - 3302.81884765625),
            deep = Vector3.new(- 1510.88672, - 237.695053, - 2852.90674),
            enchant = Vector3.new(1296.320068359375, - 808.5519409179688, - 298.93817138671875),
            executive = Vector3.new(- 29.836761474609375, - 250.48486328125, 199.11614990234375),
            keepers = Vector3.new(1296.320068359375, - 808.5519409179688, - 298.93817138671875),
            mod_house = Vector3.new(- 30.205902099609375, - 249.40594482421875, 204.0529022216797),
            moosewood = Vector3.new(383.10113525390625, 131.2406005859375, 243.93385314941406),
            mushgrove = Vector3.new(2501.486083984375, 131.00001525878906, - 720.6993408203125),
            roslit = Vector3.new(- 1476.5079345703125, 133.5, 671.6812744140625),
            snow = Vector3.new(2648.67578125, 139.06605529785156, 2521.29736328125),
            snowcap = Vector3.new(2649.06201171875, 142.28382873535156, 2521.45263671875),
            spike = Vector3.new(- 1253.3489990234375, 137.20669555664062, 1554.5740966796875),
            statue = Vector3.new(73.47272491455078, 141.92999267578125, - 1027.432373046875),
            sunstone = Vector3.new(- 932.7903442382813, 131.8808135986328, - 1119.1905517578125),
            swamp = Vector3.new(2501.592529296875, 131.00001525878906, - 720.704345703125),
            terrapin = Vector3.new(- 147.6435546875, 150.75936889648438, 1913.392822265625),
            trident = Vector3.new(- 1479.4898700000003, - 228.710632, - 2391.39307),
            vertigo = Vector3.new(- 112.00830841064453, - 515.2993774414063, 1040.327880859375),
            volcano = Vector3.new(- 1888.5234375, 167.78244018554688, 329.23529052734375),
            wilson = Vector3.new(2938.80591, 277.47476200000006, 2567.13379),
            wilsons_rod = Vector3.new(2879.2085, 135.07663, 2723.64233)
        };
        local v260 = v259[v258];
        if v260 then
            local v413 = 0;
            local v414;
            while true do
                if (v413 == 0) then
                    v414 = game.Players.LocalPlayer;
                    if (v414 and v414.Character and v414.Character:FindFirstChild('HumanoidRootPart')) then
                        v414.Character.HumanoidRootPart.CFrame = CFrame.new(v260);
                    end
                    break
                end
            end
        else
            warn('Invalid location selected!');
        end
    end
});
local v89 = v10.Teleport:AddDropdown('Teleport To Totem', {
    Title = 'Teleport To Totems',
    Description = "",
    Values = {
        'Aurora Totem',
        'Smokescreen Totem',
        'Windset Totem',
        'Tempest Totem',
        'Sundial Totem',
        'Eclipse Totem',
        'Meteor Totem',
        'Blizzard Totem',
        'Avalanche Totem'
    },
    Multi = false,
    Default = 'None',
    Callback = function(v261)
        local v262 = 0;
        local v263;
        local v264;
        while true do
            if (v262 == (0)) then
                local v482 = 0;
                while true do
                    if (v482 == (0)) then
                        v263 = {
                            ['Aurora Totem'] = Vector3.new(- 1811.0008544921875, - 136.8893280029297, - 3282.000244140625),
                            ['Smokescreen Totem'] = Vector3.new(2789, 139.8254852294922, - 625),
                            ['Windset Totem'] = Vector3.new(2849, 178.33323669433594, 2702),
                            ['Tempest Totem'] = Vector3.new(35, 132.50001525878906, 1943),
                            ['Sundial Totem'] = Vector3.new(- 1148, 134.49998474121094, - 1075),
                            ['Eclipse Totem'] = Vector3.new(5968.00048828125, 274.0086364746094, 838.1260375976563),
                            ['Meteor Totem'] = Vector3.new(- 1948, 275.3567199707031, 230),
                            ['Blizzard Totem'] = Vector3.new(20145, 742.9527587890625, 5805),
                            ['Avalanche Totem'] = Vector3.new(19710.787109375, 467.6305847167969, 6052.2626953125)
                        };
                        v264 = v263[v261];
                        v482 = 1;
                    end
                    if (v482 == 1) then
                        v262 = 1;
                        break
                    end
                end
            end
            if (v262 == 1) then
                if v264 then
                    local v559 = game.Players.LocalPlayer;
                    if (v559 and v559.Character and v559.Character:FindFirstChild('HumanoidRootPart')) then
                        v559.Character.HumanoidRootPart.CFrame = CFrame.new(v264);
                    end
                else
                    warn('Invalid item selected!');
                end
                break
            end
        end
    end
});
local v73 = v10.Teleport:AddSection('Teleport To Items');
v10.Teleport:AddParagraph({
    Title = 'Important',
    Content = "If Nothing is displayed, please ensure to click the 'Refresh' button. And To Update Item List According To Location Click On Refresh Button"
});
local v90 = game.Workspace.world.interactables;
local v91 = {};
local function v92()
    local v265 = 0;
    local v266;
    while true do
        if (0 == v265) then
            v91 = {};
            v266 = {};
            v265 = 1;
        end
        if (v265 == (1)) then
            for v525, v526 in pairs(v90:GetChildren()) do
                if v526:IsA('Model') then
                    local v601 = 0;
                    local v602;
                    while true do
                        if ((0) == v601) then
                            v602 = v526.Name;
                            if not v266[v602] then
                                local v767 = 0;
                                local v768;
                                while true do
                                    if (v767 == (0)) then
                                        v768 = 0;
                                        while true do
                                            if ((0) == v768) then
                                                table.insert(v91, v602);
                                                v266[v602] = true;
                                                break
                                            end
                                        end
                                        break
                                    end
                                end
                            end
                            break
                        end
                    end
                end
            end
            break
        end
    end
end
local v89 = v10.Teleport:AddDropdown('Dropdown', {
    Title = 'Select Item',
    Description = "",
    Values = v91,
    Multi = false,
    Default = 'None'
});
local function v93(v267)
    local v268 = Vector3.new(0, 0, 0);
    local v269 = 0;
    for v363, v364 in pairs(v267:GetDescendants()) do
        if v364:IsA('BasePart') then
            v268 += v364.Position
            v269 += (1)
        end
    end
    if (v269 > (0)) then
        return v268 / v269
    else
        return nil
    end
end
local function v94(v270)
    local v271 = 0;
    local v272;
    while true do
        if (v271 == (0)) then
            v272 = v93(v270);
            if v272 then
                local v560 = 0;
                local v561;
                local v562;
                local v563;
                while true do
                    if (v560 == 1) then
                        v563 = v562.Character or v562.CharacterAdded:Wait() ;
                        if (v563 and v563:FindFirstChild('HumanoidRootPart')) then
                            v563.HumanoidRootPart.CFrame = CFrame.new(v561);
                        else
                            warn('Player character or HumanoidRootPart not found.');
                        end
                        break
                    end
                    if (v560 == (0)) then
                        v561 = v272 + Vector3.new(0, 5, 0) ;
                        v562 = game.Players.LocalPlayer;
                        v560 = 1;
                    end
                end
            else
                warn('Could not calculate the center of the model.');
            end
            break
        end
    end
end
v89:OnChanged(function(v273)
    local v274 = 0;
    local v275;
    while true do
        if (v274 == (0)) then
            v275 = v90:FindFirstChild(v273);
            if (v275 and v275:IsA('Model')) then
                v94(v275);
            else
                warn('Selected model is invalid.');
            end
            break
        end
    end
end);
v10.Teleport:AddButton({
    Title = 'Refresh',
    Description = "",
    Callback = function()
        v92();
        v89:SetValues(v91);
    end
});
local v73 = v10.Teleport:AddSection('Teleport To Zones + Zone Events');
local v95 = game.Workspace.zones.fishing;
local function v96()
    local v276 = 0;
    local v277;
    local v278;
    while true do
        if (v276 == (0)) then
            local v483 = 0;
            while true do
                if (v483 == (1)) then
                    v276 = 1;
                    break
                end
                if (v483 == (0)) then
                    v277 = {};
                    v278 = {};
                    v483 = 1;
                end
            end
        end
        if (v276 == 1) then
            local v484 = 0;
            while true do
                if ((0) == v484) then
                    for v642, v643 in pairs(v95:GetChildren()) do
                        if v643:IsA('Part') then
                            if not v278[v643.Name] then
                                local v769 = 0;
                                while true do
                                    if (v769 == (0)) then
                                        table.insert(v277, v643.Name);
                                        v278[v643.Name] = true;
                                        break
                                    end
                                end
                            end
                        end
                    end
                    return v277
                end
            end
        end
    end
end
local function v97(v279)
    local v280 = Region3.new(v279 - Vector3.new(2, 5, 2), v279 + Vector3.new(2, 5, 2));
    local v281 = workspace:FindPartsInRegion3(v280, nil, math.huge);
    for v365, v366 in pairs(v281) do
        if v366.CanCollide then
            return false
        end
    end
    return true
end
local function v98(v282)
    local v283 = v95:FindFirstChild(v282);
    if v283 then
        local v415 = 0;
        local v416;
        while true do
            if (v415 == 1) then
                game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(v416));
                for v603, v604 in pairs(v95:GetChildren()) do
                    if v604:IsA('Part') then
                        v604.CanCollide = true;
                    end
                end
                break
            end
            if (v415 == (0)) then
                v416 = v283.Position + Vector3.new(0, 10, 0) ;
                while not v97(v416) do
                    v416 = v416 + Vector3.new(0, 1, 0) ;
                end
                v415 = 1;
            end
        end
    end
end
local function v99()
    local v284 = 0;
    local v285;
    while true do
        if (v284 == (0)) then
            v285 = game.Workspace.zones:FindFirstChild('fishing');
            if v285 then
                local v564 = 0;
                while true do
                    if (v564 == 1) then
                        v285.Parent = game.Workspace.zones;
                        break
                    end
                    if (v564 == (0)) then
                        v285.Parent = nil;
                        wait(1);
                        v564 = 1;
                    end
                end
            end
            break
        end
    end
end
local v89 = v10.Teleport:AddDropdown('Dropdown', {
    Title = 'Select Zone',
    Description = "",
    Values = v96(),
    Multi = false,
    Default = 'None',
    Callback = function(v286)
        v98(v286);
    end
});
v10.Teleport:AddButton({
    Title = 'Refresh',
    Description = "",
    Callback = function()
        v99();
    end
});
local v73 = v10.Teleport:AddSection('Teleport To Npcs');
v10.Teleport:AddParagraph({
    Title = 'Important',
    Content = "If 'No NPCs Found' is displayed, please ensure to click the 'Refresh' button. And To Update NPCS List According To Location Click On Refresh Button"
});
local v100 = game:GetService('Workspace');
local v101 = game:GetService('Players');
local v102 = v100:WaitForChild('world'):WaitForChild('npcs');
local v11 = v101.LocalPlayer;
local function v103()
    return v11.Character or v11.CharacterAdded:Wait()
end
local v104 = {};
local function v105()
    local v287 = 0;
    while true do
        if (v287 == (0)) then
            v104 = {};
            for v527, v528 in pairs(v102:GetChildren()) do
                if (v528:IsA('Model') and v528:FindFirstChild('HumanoidRootPart')) then
                    v104[v528.Name] = v528.HumanoidRootPart.Position;
                end
            end
            break
        end
    end
end
local function v106()
    local v288 = {};
    for v367 in pairs(v104) do
        table.insert(v288, v367);
    end
    if (# v288 == (0)) then
        table.insert(v288, 'No NPCs Found');
    end
    return v288
end
local v107;
local v89 = v10.Teleport:AddDropdown('Dropdown', {
    Title = 'Select NPC',
    Description = "",
    Values = v106(),
    Multi = false,
    Default = 'None',
    Callback = function(v289)
        local v290 = 0;
        while true do
            if (v290 == (0)) then
                v107 = v289;
                print('Selected NPC:', v107);
                break
            end
        end
    end
});
local function v108()
    if v107 then
        local v417 = 0;
        local v418;
        while true do
            if ((0) == v417) then
                v418 = v104[v107];
                if v418 then
                    local v644 = 0;
                    local v645;
                    while true do
                        if (v644 == (0)) then
                            v645 = v103();
                            if (v645 and v645:FindFirstChild('HumanoidRootPart')) then
                                v645.HumanoidRootPart.CFrame = CFrame.new(v418 + Vector3.new(0, 5, 0));
                            else
                                warn('humanoidRootPart not found');
                            end
                            break
                        end
                    end
                else
                    warn('Invalid NPC selected or position missing!');
                end
                break
            end
        end
    else
        warn('No NPC selected!');
    end
end
v10.Teleport:AddButton({
    Title = 'Teleport',
    Description = "",
    Callback = function()
        v108();
    end
});
v10.Teleport:AddButton({
    Title = 'Refresh',
    Description = "",
    Callback = function()
        local v291 = 0;
        local v292;
        while true do
            if (v291 == (1)) then
                v89:SetValues(v292);
                print('NPCs refreshed!');
                break
            end
            if (v291 == (0)) then
                v105();
                v292 = v106();
                v291 = 1;
            end
        end
    end
});
local v73 = v10.Teleport:AddSection('Teleport To Players');
local v101 = game:GetService('Players');
local function v109()
    local v293 = 0;
    local v294;
    while true do
        if (v293 == 1) then
            return v294
        end
        if (v293 == (0)) then
            v294 = {};
            for v529, v530 in ipairs(v101:GetPlayers()) do
                table.insert(v294, v530.Name);
            end
            v293 = 1;
        end
    end
end
local v89 = v10.Teleport:AddDropdown('Dropdown', {
    Title = 'Select Player',
    Description = "",
    Values = v109(),
    Multi = false,
    Default = 'None'
});
v10.Teleport:AddButton({
    Title = 'Teleport',
    Description = "",
    Callback = function()
        local v295 = 0;
        local v296;
        while true do
            if (v295 == (0)) then
                v296 = v89.Value;
                if v296 then
                    local v566 = v101:FindFirstChild(v296);
                    if v566 then
                        local v646 = 0;
                        local v647;
                        while true do
                            if (v646 == (0)) then
                                v647 = v566.Character;
                                if (v647 and v647:FindFirstChild('HumanoidRootPart')) then
                                    local v811 = v101.LocalPlayer;
                                    local v812 = v811.Character;
                                    if (v812 and v812:FindFirstChild('HumanoidRootPart')) then
                                        v811.Character:SetPrimaryPartCFrame(v647.HumanoidRootPart.CFrame);
                                    else
                                        warn('character not found');
                                    end
                                else
                                    warn("player doesn't have a valid humanoidrootpart");
                                end
                                break
                            end
                        end
                    else
                        warn('selected player not found in game');
                    end
                else
                    warn('No player selected from the dropdown');
                end
                break
            end
        end
    end
});
v10.Teleport:AddButton({
    Title = 'Refresh',
    Description = "",
    Callback = function()
        local v297 = v109();
        v89:SetValues(v297);
    end
});
local v73 = v10.Performance:AddSection('Recommended only for low-end devices');
local v34 = v10.Performance:AddSlider('FPSCAP', {
    Title = 'FPS',
    Description = "",
    Default = 60,
    Min = 1,
    Max = 4000,
    Rounding = 1,
    Callback = function(v298)
        setfpscap(tonumber(v298));
    end
});
v10.Performance:AddButton({
    Title = 'Anti Lag (1)',
    Description = "",
    Callback = function()
        local v299 = true;
        local v300 = game;
        local v301 = v300.Workspace;
        local v302 = v300.Lighting;
        local v303 = v301.Terrain;
        v303.WaterWaveSize = 0;
        v303.WaterWaveSpeed = 0;
        v303.WaterReflectance = 0;
        v303.WaterTransparency = 0;
        v302.GlobalShadows = false;
        v302.FogEnd = 8999999488;
        v302.Brightness = 0;
        settings().Rendering.QualityLevel = 'Level01';
        for v368, v369 in pairs(v300:GetDescendants()) do
            if (v369:IsA('Part') or v369:IsA('Union') or v369:IsA('CornerWedgePart') or v369:IsA('TrussPart')) then
                local v486 = 0;
                while true do
                    if (v486 == 0) then
                        v369.Material = 'Plastic';
                        v369.Reflectance = 0;
                        break
                    end
                end
            elseif (v369:IsA('Decal') or (v369:IsA('Texture') and v299)) then
                v369.Transparency = 1;
            elseif (v369:IsA('ParticleEmitter') or v369:IsA('Trail')) then
                v369.Lifetime = NumberRange.new(0);
            elseif v369:IsA('Explosion') then
                v369.BlastPressure = 1;
                v369.BlastRadius = 1;
            elseif (v369:IsA('Fire') or v369:IsA('SpotLight') or v369:IsA('Smoke')) then
                v369.Enabled = false;
            elseif v369:IsA('MeshPart') then
                v369.Material = 'Plastic';
                v369.Reflectance = 0;
                v369.TextureID = 10385902758728956;
            end
        end
        for v370, v371 in pairs(v302:GetChildren()) do
            if (v371:IsA('BlurEffect') or v371:IsA('SunRaysEffect') or v371:IsA('ColorCorrectionEffect') or v371:IsA('BloomEffect') or v371:IsA('DepthOfFieldEffect')) then
                v371.Enabled = false;
            end
        end
        print('Anti Lag settings applied lil nigga');
    end
});
local v101 = game:GetService('Players');
local v11 = v101.LocalPlayer;
local function v110(v312)
    if v312 then
        for v488, v489 in ipairs(v312:GetDescendants()) do
            if (v489:IsA('BasePart') and (v489.Name ~= 'HumanoidRootPart')) then
                local v568 = 0;
                while true do
                    if (v568 == 0) then
                        v489.Transparency = 1;
                        v489.CanCollide = false;
                        break
                    end
                end
            elseif v489:IsA('Decal') then
                v489.Transparency = 1;
            elseif (v489:IsA('Accessory') and v489:FindFirstChild('Handle')) then
                local v744 = 0;
                local v745;
                while true do
                    if (v744 == (0)) then
                        v745 = 0;
                        while true do
                            if ((0) == v745) then
                                v489.Handle.Transparency = 1;
                                v489.Handle.CanCollide = false;
                                break
                            end
                        end
                        break
                    end
                end
            end
        end
    end
end
local function v111(v313)
    if v313 then
        for v490, v491 in ipairs(v313:GetDescendants()) do
            if (v491:IsA('BasePart') and (v491.Name ~= 'HumanoidRootPart')) then
                local v569 = 0;
                while true do
                    if (v569 == (0)) then
                        v491.Transparency = 0;
                        v491.CanCollide = true;
                        break
                    end
                end
            elseif v491:IsA('Decal') then
                v491.Transparency = 0;
            elseif (v491:IsA('Accessory') and v491:FindFirstChild('Handle')) then
                v491.Handle.Transparency = 0;
                v491.Handle.CanCollide = true;
            end
        end
    end
end
v10.Performance:AddButton({
    Title = 'Anti Lag (2)',
    Description = "",
    Callback = function()
        for v372, v373 in pairs(game:GetDescendants()) do
            if (v373:IsA('Part') or v373:IsA('UnionOperation') or v373:IsA('MeshPart')) then
                if (v373.Transparency ~= (1)) then
                    v373.Material = Enum.Material.SmoothPlastic;
                end
            elseif (v373:IsA('ParticleEmitter') or v373:IsA('Trail')) then
                v373:Destroy();
            end
        end
        print('Anti Lag Success');
    end
});
v10.Performance:AddButton({
    Title = 'Destroy All Particle',
    Description = "",
    Callback = function()
        local v314 = 0;
        while true do
            if (v314 == (0)) then
                for v531, v532 in pairs(game:GetDescendants()) do
                    if (v532:IsA('ParticleEmitter') or v532:IsA('Trail')) then
                        v532:Destroy();
                    end
                end
                print('Success Destroy Particle');
                break
            end
        end
    end
});
local v112 = v10.Performance:AddToggle('HidePlayersToggle', {
    Title = 'Hide Other Players',
    Description = "",
    Default = false,
    Callback = function(v315)
        for v374, v375 in ipairs(v101:GetPlayers()) do
            if (v375 ~= v11) then
                v375.CharacterAdded:Connect(function(v533)
                    if v315 then
                        v110(v533);
                    else
                        v111(v533);
                    end
                end);
                if v375.Character then
                    if v315 then
                        v110(v375.Character);
                    else
                        v111(v375.Character);
                    end
                end
            end
        end
    end
});
local function v113()
    local v316 = game.Workspace;
    local v317 = game.Lighting;
    local v318 = v316.Terrain;
    v318.WaterWaveSize = 0;
    v318.WaterWaveSpeed = 0;
    v318.WaterReflectance = 0;
    v318.WaterTransparency = 0;
    v317.GlobalShadows = false;
    v317.FogEnd = 8999999488;
    v317.Brightness = 0;
    settings().Rendering.QualityLevel = 'Level01';
    for v376, v377 in pairs(game:GetDescendants()) do
        if (v377:IsA('BasePart') or v377:IsA('MeshPart')) then
            local v492 = 0;
            while true do
                if (v492 == (1)) then
                    v377.CastShadow = false;
                    break
                end
                if (v492 == 0) then
                    v377.Material = 'SmoothPlastic';
                    v377.Reflectance = 0;
                    v492 = 1;
                end
            end
        elseif v377:IsA('Decal') then
            v377.Transparency = 1;
        elseif (v377:IsA('ParticleEmitter') or v377:IsA('Trail')) then
            v377.Lifetime = NumberRange.new(0);
        elseif v377:IsA('Explosion') then
            v377.BlastPressure = 1;
            v377.BlastRadius = 1;
        elseif (v377:IsA('Fire') or v377:IsA('SpotLight') or v377:IsA('Smoke')) then
            v377.Enabled = false;
        end
    end
    for v378, v379 in pairs(v317:GetChildren()) do
        if (v379:IsA('PostEffect') or v379:IsA('DepthOfFieldEffect')) then
            v379.Enabled = false;
        end
    end
end
v10.Performance:AddButton({
    Title = '1-Click FPS Boost',
    Description = "",
    Callback = function()
        v113();
    end
});
local v39 = v10.ESP:AddToggle('ItemESP', {
    Title = 'Item ESP',
    Description = "",
    Default = false,
    Callback = function(v327)
        local v328 = game.Workspace:FindFirstChild('world');
        if not v328 then
            warn('world folder not found in Workspace');
            return
        end
        local v329 = v328:FindFirstChild('interactables');
        if not v329 then
            local v419 = 0;
            while true do
                if (v419 == (0)) then
                    warn('interactables folder not found in world');
                    return
                end
            end
        end
        if v327 then
            for v494, v495 in pairs(v329:GetChildren()) do
                if v495:IsA('Model') then
                    local v573 = Instance.new('Highlight');
                    v573.Parent = v495;
                    v573.Adornee = v495;
                    v573.FillColor = Color3.fromRGB(255, 0, 0);
                    v573.OutlineColor = Color3.fromRGB(255, 255, 255);
                    v573.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop;
                    local v580 = v495.PrimaryPart or v495:FindFirstChild('PrimaryPart') ;
                    if v580 then
                        local v652 = Instance.new('BillboardGui');
                        v652.Parent = v580;
                        v652.Adornee = v580;
                        v652.Size = UDim2.new(4, 0, 1, 0);
                        v652.StudsOffset = Vector3.new(0, 2.5, 0);
                        v652.AlwaysOnTop = true;
                        local v658 = Instance.new('TextLabel');
                        v658.Parent = v652;
                        v658.Size = UDim2.new(1, 0, 2, 0);
                        v658.BackgroundTransparency = 1;
                        v658.Text = v495.Name;
                        v658.TextColor3 = Color3.fromRGB(255, 255, 255);
                        v658.TextStrokeTransparency = 0;
                        v658.TextStrokeColor3 = Color3.fromRGB(0, 0, 0);
                        v658.Font = Enum.Font.GothamBold;
                        v658.TextScaled = true;
                    end
                end
            end
            print('Toggle On - Item ESP Enabled');
        else
            local v420 = 0;
            while true do
                if ((0) == v420) then
                    for v612, v613 in pairs(v329:GetChildren()) do
                        if v613:IsA('Model') then
                            local v693 = 0;
                            local v694;
                            local v695;
                            while true do
                                if ((1) == v693) then
                                    v695 = v613.PrimaryPart or v613:FindFirstChild('PrimaryPart') ;
                                    if v695 then
                                        local v819 = 0;
                                        local v820;
                                        while true do
                                            if (v819 == (0)) then
                                                v820 = v695:FindFirstChildOfClass('BillboardGui');
                                                if v820 then
                                                    v820:Destroy();
                                                end
                                                break
                                            end
                                        end
                                    end
                                    break
                                end
                                if (v693 == 0) then
                                    local v772 = 0;
                                    while true do
                                        if (v772 == (0)) then
                                            v694 = v613:FindFirstChildOfClass('Highlight');
                                            if v694 then
                                                v694:Destroy();
                                            end
                                            v772 = 1;
                                        end
                                        if (v772 == 1) then
                                            v693 = 1;
                                            break
                                        end
                                    end
                                end
                            end
                        end
                    end
                    print('Toggle Off');
                    break
                end
            end
        end
    end
});
local v39 = v10.ESP:AddToggle('NPCESP', {
    Title = 'NPC ESP',
    Description = "",
    Default = false,
    Callback = function(v330)
        local v331 = game.Workspace:FindFirstChild('world');
        if not v331 then
            warn('world folder not found in Workspace');
            return
        end
        local v332 = v331:FindFirstChild('npcs');
        if not v332 then
            local v421 = 0;
            while true do
                if (v421 == (0)) then
                    warn('npcs folder not found in world');
                    return
                end
            end
        end
        if v330 then
            for v496, v497 in pairs(v332:GetChildren()) do
                if (v497:IsA('Model') and v497:FindFirstChild('HumanoidRootPart')) then
                    local v581 = 0;
                    local v582;
                    local v583;
                    local v584;
                    while true do
                        if (v581 == 3) then
                            v583.StudsOffset = Vector3.new(0, 2.5, 0);
                            v583.AlwaysOnTop = true;
                            v584 = Instance.new('TextLabel');
                            v581 = 4;
                        end
                        if (v581 == (0)) then
                            v582 = Instance.new('Highlight');
                            v582.Parent = v497;
                            v582.Adornee = v497;
                            v581 = 1;
                        end
                        if (v581 == (5)) then
                            v584.Text = v497.Name;
                            v584.TextColor3 = Color3.fromRGB(255, 255, 255);
                            v584.TextStrokeTransparency = 0;
                            v581 = 6;
                        end
                        if ((4) == v581) then
                            v584.Parent = v583;
                            v584.Size = UDim2.new(1, 0, 2, 0);
                            v584.BackgroundTransparency = 1;
                            v581 = 5;
                        end
                        if (v581 == (1)) then
                            v582.FillColor = Color3.fromRGB(0, 255, 0);
                            v582.OutlineColor = Color3.fromRGB(255, 255, 255);
                            v583 = Instance.new('BillboardGui');
                            v581 = 2;
                        end
                        if (v581 == (2)) then
                            v583.Parent = v497.HumanoidRootPart;
                            v583.Adornee = v497.HumanoidRootPart;
                            v583.Size = UDim2.new(4, 0, 1, 0);
                            v581 = 3;
                        end
                        if (v581 == (6)) then
                            v584.TextStrokeColor3 = Color3.fromRGB(0, 0, 0);
                            v584.Font = Enum.Font.GothamBold;
                            v584.TextScaled = true;
                            break
                        end
                    end
                end
            end
            print('Toggle On');
        else
            local v422 = 0;
            while true do
                if (v422 == 0) then
                    for v614, v615 in pairs(v332:GetChildren()) do
                        if (v615:IsA('Model') and v615:FindFirstChild('HumanoidRootPart')) then
                            local v717 = 0;
                            local v718;
                            local v719;
                            while true do
                                if (v717 == 0) then
                                    v718 = v615:FindFirstChildOfClass('Highlight');
                                    if v718 then
                                        v718:Destroy();
                                    end
                                    v717 = 1;
                                end
                                if (v717 == (1)) then
                                    v719 = v615.HumanoidRootPart:FindFirstChildOfClass('BillboardGui');
                                    if v719 then
                                        v719:Destroy();
                                    end
                                    break
                                end
                            end
                        end
                    end
                    print('Toggle Off');
                    break
                end
            end
        end
    end
});
local v39 = v10.ESP:AddToggle('PlayerESP', {
    Title = 'Player ESP',
    Description = "",
    Default = false,
    Callback = function(v333)
        if v333 then
            local v423 = 0;
            while true do
                if (v423 == (0)) then
                    for v616, v617 in pairs(game.Players:GetPlayers()) do
                        if (v617.Character and v617.Character:FindFirstChild('HumanoidRootPart')) then
                            local v720 = 0;
                            local v721;
                            local v722;
                            local v723;
                            local v724;
                            local v725;
                            local v726;
                            local v727;
                            local v728;
                            while true do
                                if (v720 == (1)) then
                                    v723.FillColor = Color3.fromRGB(0, 255, 0);
                                    v723.OutlineColor = Color3.fromRGB(255, 255, 255);
                                    v723.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop;
                                    v723.Enabled = true;
                                    v724 = Instance.new('BillboardGui');
                                    v720 = 2;
                                end
                                if (v720 == 5) then
                                    local v778 = 0;
                                    while true do
                                        if (v778 == 2) then
                                            v723.OutlineTransparency = 0.5;
                                            v720 = 6;
                                            break
                                        end
                                        if (v778 == (1)) then
                                            v728 = math.min(15, math.max(5, v727 / 50));
                                            v724.Size = UDim2.new(v728, 0, 3, 0);
                                            v778 = 2;
                                        end
                                        if (v778 == (0)) then
                                            v726 = game.Workspace.CurrentCamera;
                                            v727 = (v726.CFrame.Position - v722.Position).Magnitude;
                                            v778 = 1;
                                        end
                                    end
                                end
                                if (v720 == (3)) then
                                    local v779 = 0;
                                    while true do
                                        if (v779 == (0)) then
                                            v725 = Instance.new('TextLabel');
                                            v725.Parent = v724;
                                            v779 = 1;
                                        end
                                        if (v779 == (1)) then
                                            v725.Size = UDim2.new(1, 0, 1, 0);
                                            v725.BackgroundTransparency = 1;
                                            v779 = 2;
                                        end
                                        if ((2) == v779) then
                                            v725.Text = v617.Name;
                                            v720 = 4;
                                            break
                                        end
                                    end
                                end
                                if (v720 == 6) then
                                    v723.FillTransparency = 0.5;
                                    break
                                end
                                if (v720 == (2)) then
                                    v724.Parent = v722;
                                    v724.Adornee = v722;
                                    v724.Size = UDim2.new(6, 0, 1.5, 0);
                                    v724.StudsOffset = Vector3.new(0, 5, 0);
                                    v724.AlwaysOnTop = true;
                                    v720 = 3;
                                end
                                if (v720 == (4)) then
                                    v725.TextColor3 = Color3.fromRGB(255, 255, 255);
                                    v725.TextStrokeTransparency = 0;
                                    v725.TextStrokeColor3 = Color3.fromRGB(0, 0, 0);
                                    v725.Font = Enum.Font.GothamBold;
                                    v725.TextScaled = true;
                                    v720 = 5;
                                end
                                if (v720 == (0)) then
                                    v721 = v617.Character;
                                    v722 = v721:FindFirstChild('HumanoidRootPart');
                                    v723 = Instance.new('Highlight');
                                    v723.Parent = v721;
                                    v723.Adornee = v721;
                                    v720 = 1;
                                end
                            end
                        end
                    end
                    print('Toggle On');
                    break
                end
            end
        else
            for v498, v499 in pairs(game.Players:GetPlayers()) do
                if (v499.Character and v499.Character:FindFirstChild('HumanoidRootPart')) then
                    local v585 = 0;
                    local v586;
                    local v587;
                    local v588;
                    local v589;
                    while true do
                        if (v585 == (1)) then
                            v588 = v586:FindFirstChildOfClass('Highlight');
                            if v588 then
                                v588:Destroy();
                            end
                            v585 = 2;
                        end
                        if (v585 == (0)) then
                            v586 = v499.Character;
                            v587 = v586:FindFirstChild('HumanoidRootPart');
                            v585 = 1;
                        end
                        if (v585 == (2)) then
                            v589 = v587:FindFirstChildOfClass('BillboardGui');
                            if v589 then
                                v589:Destroy();
                            end
                            break
                        end
                    end
                end
            end
            print('Toggle Off');
        end
    end
});
local v73 = v10.STATS:AddSection('                                Player Stats :');
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v119 = v118:WaitForChild('spawnlocation');
v10.STATS:AddParagraph({
    Title = 'Spawn Location',
    Content = 'Spawn Location: ' .. v119.Value
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v120 = v118:WaitForChild('title');
v10.STATS:AddParagraph({
    Title = 'Title',
    Content = 'Title: ' .. v120.Value
});
local v114 = game.Players.LocalPlayer;
local v121 = v114.leaderstats.Level.Value;
v10.STATS:AddParagraph({
    Title = 'Your Current Level',
    Content = 'Level : ' .. tostring(v121)
});
local v114 = game.Players.LocalPlayer;
local v122 = v114.leaderstats['C$'].Value;
v10.STATS:AddParagraph({
    Title = 'Your Current Cash',
    Content = 'Cash : ' .. tostring(v122)
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v123 = v118:WaitForChild('tracker_timeplayed');
local v124 = v123.Value;
local v125 = math.floor(v124 / 3600);
local v126 = math.floor((v124 % (36E2)) / 60);
local v127 = v124 % (60) ;
local v128 = string.format('%02d:%02d:%02d', v125, v126, v127);
v10.STATS:AddParagraph({
    Title = 'Time Played',
    Content = 'Total Time Played: ' .. v128
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v129 = v118:WaitForChild('tracker_timesjoined');
local v130 = v129.Value;
v10.STATS:AddParagraph({
    Title = 'Times Joined',
    Content = 'Total Times Joined: ' .. tostring(v130)
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v131 = v118:WaitForChild('dailystreak');
local v132 = v131.Value;
v10.STATS:AddParagraph({
    Title = 'Daily Streak',
    Content = 'Current Daily Streak: ' .. tostring(v132)
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v133 = v118:WaitForChild('tracker_fishcaught');
local v134 = v133.Value;
v10.STATS:AddParagraph({
    Title = 'Total Fishes Caught',
    Content = 'Total Fishes Caught: ' .. tostring(v134)
});
local v114 = game.Players.LocalPlayer;
local v115 = game:GetService('ReplicatedStorage');
local v116 = v115:WaitForChild('playerstats');
local v117 = v116:WaitForChild(v114.Name);
local v118 = v117:WaitForChild('Stats');
local v135 = v118:WaitForChild('tracker_deaths');
local v136 = v135.Value;
v10.STATS:AddParagraph({
    Title = 'Total Deaths',
    Content = 'Total Deaths: ' .. tostring(v136)
});
local v73 = v10.STATS:AddSection('                                Server Info :');
local v137 = game.JobId;
local v138 = game:GetService('ReplicatedStorage'):WaitForChild('world'):WaitForChild('region_country');
local v139 = v138.Value;
local v140 = game:GetService('ReplicatedStorage'):WaitForChild('world'):WaitForChild('region_city');
local v141 = v140.Value;
local v142 = game:GetService('ReplicatedStorage'):WaitForChild('world'):WaitForChild('region_region');
local v143 = v142.Value;
local v114 = game.Players.LocalPlayer;
local v144 = game:GetService('ReplicatedStorage'):WaitForChild('playerstats'):WaitForChild(v114.Name):WaitForChild('Stats'):WaitForChild('lastversion');
local v145 = v144.Value;
local v146 = game:GetService('MarketplaceService');
local v147, v148 = pcall(function()
    return v146:GetProductInfo(game.PlaceId)
end);
local v149 = 'Unknown';
if (v147 and v148) then
    v149 = v148.Name;
end
local v150 = game.PlaceId;
local v151 = game:GetService('UserInputService');
local v152 = v151:GetPlatform().Name;
v73:AddParagraph({
    Title = 'Server ID: ' .. v137
});
v73:AddParagraph({
    Title = 'Server Region: ' .. v139
});
v73:AddParagraph({
    Title = 'Server City: ' .. v141
});
v73:AddParagraph({
    Title = 'Server Region Region: ' .. v143
});
v73:AddParagraph({
    Title = 'Current Game Version: ' .. v145
});
v73:AddParagraph({
    Title = 'Game Name: ' .. v149
});
v73:AddParagraph({
    Title = 'Place ID: ' .. v150
});
v73:AddParagraph({
    Title = 'Platform: ' .. v152
});
local v73 = v10.info:AddSection('Info + Fixes');
v10.info:AddParagraph({
    Title = 'How To Fix Blur Problem ?',
    Content = "To Fix Blur Problem Set Your Graphics Quality\nTo 7 or Below 7"
});
v10.info:AddParagraph({
    Title = 'New Updates!',
    Content = 'We will keep updating this with many amazing features in the future. Have any suggestions? Join our Discord and let us know!'
});
