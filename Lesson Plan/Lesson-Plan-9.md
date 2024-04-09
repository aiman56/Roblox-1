<link rel="stylesheet" type="text/css" href="styles.css" />

# Roblox  1 : Sound Design <!-- omit from toc -->

<hr>    


## Table of Contents <!-- omit from toc -->
- [Sounds](#sounds)

## Sounds

Sounds make games more exciting. They include everything from music to noises like footsteps or explosions. These sounds help set the scene and make the game feel real. Developers can pick from lots of different sounds to make their games more fun and interesting. Whether it's the sound of a car engine or birds chirping in the background, sounds bring Roblox worlds to life and make them more enjoyable to play in.

We can use a ready made ***Sounds*** similar to how we did it in our past lesson for ***Models***. 

1. Open the ***Toolbox*** from the ***Home*** tab and choose ***Audio*** from the dropdown menu.

<p align="center">
    <img src="..\Assets\drawing91.png" alt="drawing91"  width="400" style="border: 2px solid  gray;"/>
</p>

2. You can search the sound that you like searching the theme in the ***Search*** bar.

3. To add the sounds to the ***Workspace***, first <kbd>Left Mouse Click</kbd> on the ***Workspace*** in the ***Explorer*** window until it is highlighted.

<p align="center">
    <img src="..\Assets\drawing92.png" alt="drawing92"  width="300" style="border: 2px solid  gray;"/>
</p>

4. Then, double <kbd>Left Mouse Click</kbd> on the sounds in the list, you can see the sounds will appear in the ***Workspace***.

<p align="center">
    <img src="..\Assets\drawing93.png" alt="drawing93"  width="300" style="border: 2px solid  gray; margin-right: 60px;"/>
    <img src="..\Assets\drawing94.png" alt="drawing94"  width="300" style="border: 2px solid  gray;"/>
</p>

## Background Sound

Background music serves as a powerful tool to enhance the atmosphere and immersion of a game environment. By incorporating carefully selected audio tracks, developers can set the tone, evoke emotions, and create memorable experiences for players.

1. Get the ``assetID`` of the sounds that you like, to do this, search the sounds as shown before. Click on the sounds and click the ***+*** on the right side of the sounds. Then, click the options on the botton left and choose ***Copy Asset ID***.

<p align="center">
    <img src="..\Assets\drawing95.png" alt="drawing95"  width="300" style="border: 2px solid  gray;"/>
    
</p>

<p align="center">
    <img src="..\Assets\drawing96.png" alt="drawing96"  width="300" style="border: 2px solid  gray;"/>
</p>

2. Navigate to ***StarterPack -> StarterPlayerScripts***  in the ***Explorer*** window and add ***LocalScript***.

3. Inside the ***LocalScript***, we can add the code to play the background sound when we enter the game. Remember to repalce the ```SoundId``` to your asset's respective assedID that you have copied.

```Lua
local backgroundMusic = Instance.new("Sound")
backgroundMusic.SoundId = "rbxassetid://YOUR_BACKGROUND_MUSIC_ID_HERE" -- Replace YOUR_BACKGROUND_MUSIC_ID_HERE with the ID of the background music
backgroundMusic.Looped = true
backgroundMusic.Volume = 0.5 -- Adjust the volume as desired
backgroundMusic.Parent = game.Workspace -- Parent the sound to Workspace to ensure it plays throughout the game

-- Play the background music
backgroundMusic:Play()
```

## Proximity Sounds

Proximity sounds in Roblox games are like invisible storytellers . They're the sounds you hear when you get close to certain things in the game. For example, when you near a waterfall, you might hear the rush of water getting louder. Or when you approach a spooky cave, you might hear eerie echoes. 

1. Navigate to any ***Parts*** in the ***Workspace*** and a ***Script***.

2. Get the ``assetID`` of the sounds that you want to add to the ***Part***.

3. Define the script and paste the ``assetID`` of the sounds that you have chosen.

```Lua
-- Define the Part and the Sound
local part = script.Parent
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://5476307813" -- Replace YOUR_SOUND_ID_HERE with the ID of the sound you want to use
sound.Parent = part
```

4. Establish the distance of sounds that you want to play and also create a function to chech if a ***Player*** is nearby.

```Lua
-- Define the Part and the Sound
local part = script.Parent
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://5476307813" -- Replace YOUR_SOUND_ID_HERE with the ID of the sound you want to use
sound.Parent = part

-- Set up proximity detection
local proximityRadius = 10 -- Adjust the radius as needed
local debounce = false

-- Function to check if a Player is nearby
local function checkPlayerNearby()
	local players = game.Players:GetPlayers()
	for _, player in ipairs(players) do
		if (player.Character and (player.Character.HumanoidRootPart.Position - part.Position).magnitude <= proximityRadius) then
			return true
		end
	end
	return false
end

```

5. Add the function to play the sounds when ***Player*** is nearby and connect the function to the service.

```Lua
-- Define the Part and the Sound
local part = script.Parent
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://5476307813" -- Replace YOUR_SOUND_ID_HERE with the ID of the sound you want to use
sound.Parent = part

-- Set up proximity detection
local proximityRadius = 10 -- Adjust the radius as needed
local debounce = false

-- Function to check if a Player is nearby
local function checkPlayerNearby()
	local players = game.Players:GetPlayers()
	for _, player in ipairs(players) do
		if (player.Character and (player.Character.HumanoidRootPart.Position - part.Position).magnitude <= proximityRadius) then
			return true
		end
	end
	return false
end

-- Function to play the sound when a Player is nearby
local function playSoundNearby()
	if not debounce and checkPlayerNearby() then
		sound:Play()
		debounce = true
		wait(1) -- Adjust the wait time as needed to prevent rapid triggering
		debounce = false
	end
end

-- Connect the playSoundNearby function to the Heartbeat event
game:GetService("RunService").Heartbeat:Connect(playSoundNearby)
```




