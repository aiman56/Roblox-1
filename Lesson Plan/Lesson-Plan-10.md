<link rel="stylesheet" type="text/css" href="styles.css" />

# Roblox  1 : Racing Game <!-- omit from toc -->

<hr>    

## Table of Contents <!-- omit from toc -->
- [Creating Our Own Game](#creating-our-own-game)
- [Map Design](#map-design)
  - [Designing Race Track](#designing-race-track)
  - [Environment Design](#environment-design)
- [Visual and Audio Effect](#visual-and-audio-effect)
  - [Audio Effect](#audio-effect)
  - [Visual Effect](#visual-effect)

## Creating Our Own Game

When we make our own game, we go through different steps. First, we plan how it will work and what it will look and sound like. Then, we start building it, making sure everything works well. After that, we test it to fix any problems and make it better. Finally, we have a game that people can play and enjoy!

We are going to create our own full game, a racing game. Making a racing game means coming up with a cool idea, drawing and planning out the game, writing the code to make it work, adding awesome pictures and sounds, checking to make sure everything’s fun and works right, and then sharing it with people to play. After that, you keep making it better based on what players say. It’s like building a toy car, but in the computer world, and you’re making sure it’s super fun to play with!

## Map Design

For a racing game, we can divide our map design into two parts. The first part is designing the track that we are going to race in and the second part it creating a nice environment and terrain that suits the game theme. 

### Designing Race Track

A race track comprise of many models that includes, the road itself, barrier surrounding the road, tunnels, bridges and many more. In this example, we are going to show you some of them but you are free to anything that you like to make it more interesting.

1. Create a new Project and choose the ***Flat Terrain*** template.
   
2. Go to ***Home -> Toolbox*** , set the options to ***Model*** and search **Road**. In the search result, you will see a lot of ready-made models of road, barier, tunnels and bridge. Choose one straight road, one turn road, one bridge, one tunnel and one barrier. Make sure that you only click each model one time so that only one copy of the model will appear in the map. We will copy and paste those model again as needed in a moment to build our full track.
   
3. Once you already have all of the component in the map, carefully put barriers along both sides in the straight road model and the turn road model. Copy and paste the barrier as needed.

<p align="center">
    <img src="..\Assets\drawing102.png" alt="drawing102"  width="400" style="border: 2px solid  gray;"/>
</p>
<p align="center">
    <img src="..\Assets\drawing103.png" alt="drawing103"  width="400" style="border: 2px solid  gray;"/>
</p>

4. For both the straight road and turn road, go the map, highlight them together with the barrier on them. Right cick and choose ***Group as a Model***. You need to group the straight road with its barrier and the turn road with its barrier. Afterwards, rename the ***Model*** to ***Straight Road*** and ***Turn Road*** respectively.

5. Arrange the road in the design that you like by copy and pasting the road model that we just made. Use the tools in ***Home*** to help you in designing the track. You might notice that the grass is sticking out to the surface of the road. For now, you can ignore it first and we will resolve it later.

<p align="center">
    <img src="..\Assets\drawing101.png" alt="drawing101"  width="400" style="border: 2px solid  gray;"/>
</p>

6. For bridges, use the ***Home -> Move*** to make the road surface of the bridge to level with the surface of other road. It will be submerged underground for this step but we will put appropriate enviroments around it later.

<p align="center">
    <img src="..\Assets\drawing104.png" alt="drawing104"  width="400" style="border: 2px solid  gray;"/>
</p>


7. For the tunnel, just include it in the design as usual. Similar to bridges, we will add the environments later.


### Environment Design

It important that we include appropriate terrain and environment design to the game. incorporating suitable terrain and environment design is crucial for creating an engaging and immersive game. Thoughtful environment design not only enhances the visual appeal but also significantly impacts gameplay, providing players with a sense of place and context. It’s about selecting the right textures, colors, and structures that fit the game’s theme and challenge the player’s skills.

1. To build a hill around a tunnel we can use the ***Sculpt*** tool in the ***Terrain Editor***. You can find ***Terrain Editor*** in the ***Home*** tab.

2. Set the Brush Mode to ***Add*** and increase the Brush Size to **40**.

<p align="center">
    <img src="..\Assets\drawing105.png" alt="drawing105"  width="200" style="border: 2px solid  gray;"/>
</p>

3. Change the Material Settings to anything that you like. In this example grass was chosen.

<p align="center">
    <img src="..\Assets\drawing106.png" alt="drawing106"  width="200" style="border: 2px solid  gray;"/>
</p>

4. Click and hold the <kbd> Left Mouse Button </kbd> around the tunnel until you covered the tunnel as a whole. Do not worry if there are new terrain formed inside the tunnel. 
   
<p align="center">
    <img src="..\Assets\drawing107.png" alt="drawing107"  width="400" style="border: 2px solid  gray;"/>
</p>

5. To remove the new terrain inside the tunnel, use the ***Draw*** tool in the ***Terrain Editor***. Set the Brush Setting to subtract and change the value of Brush Size to 5.

<p align="center">
    <img src="..\Assets\drawing111.png" alt="drawing111"  width="400" style="border: 2px solid  gray;"/>
</p>

<div class="page"/>

6. To create a pool under the bridge, first we need create a hole under the bridge. To do this, use the same ***Draw*** tool as before but change the Brush Size to 10. Create the hole only under the bridge and dont remove the terrain under the normal road.

<p align="center">
    <img src="..\Assets\drawing108.png" alt="drawing108"  width="400" style="border: 2px solid  gray;"/>
</p>

7. To add water under the bridge use the ***Fill*** tool in the ***Terrain Editor*** and make sure that the boxes cover all of the hole. It is okay if the box is bigger that the hole but carefull not to increase the height too much that the bridge will be submerged.

<p align="center">
    <img src="..\Assets\drawing109.png" alt="drawing109"  width="400" style="border: 2px solid  gray;"/>
</p>

8. When you have finished putting the box at the right position,click ***Apply*** in the ***Fill*** tool.

<p align="center">
    <img src="..\Assets\drawing110.png" alt="drawing110"  width="400" style="border: 2px solid  gray;"/>
</p>

<div class="page"/>

## Visual and Audio Effect

### Audio Effect

Immerse yourself more deeply in Roblox racing games by adding background sound. With engine noises, tire screeches, and trackside sounds, the races feel more real and exciting. Whether you're speeding around sharp turns or racing down straight paths, the added sounds make the experience more intense.

1. To add background sound, you can follow the steps in our past lesson. First add a ***LocalScript*** in ***StarterPlayerScript***. 

2. Inside the ***LocalScript***, we can add the code to play the background sound when we enter the game. Remember to replace the ```SoundId``` to your asset's respective assedID that you have copied from the ***Toolbox***.

```Lua
local backgroundMusic = Instance.new("Sound")
backgroundMusic.SoundId = "rbxassetid://YOUR_BACKGROUND_MUSIC_ID_HERE" -- Replace YOUR_BACKGROUND_MUSIC_ID_HERE with the ID of the background music
backgroundMusic.Looped = true
backgroundMusic.Volume = 0.5 -- Adjust the volume as desired
backgroundMusic.Parent = game.Workspace -- Parent the sound to Workspace to ensure it plays throughout the game

-- Play the background music
backgroundMusic:Play()
```


4. To add sound everytime you press a key, add this code the the same file as the background sound script. In this example, the  key <kbd>W</kbd> is used but you can change the key to anything that you like

```Lua
local triggerSoundId = "rbxassetid://987654321" -- Replace with the actual SoundId of your trigger sound

local function playTriggerSound()
    local triggerSound = Instance.new("Sound")
    triggerSound.SoundId = triggerSoundId
    triggerSound.Volume = 0.5 -- Adjust the volume as needed
    triggerSound.Parent = game.Workspace
    triggerSound:Play()
end

-- Event handler for keyboard button press
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.W then
        playTriggerSound()
    end
end) 
```

### Visual Effect

We also want to make every part of the road that we are currently on, is glowing to make the game looks more fun. To do this:

1. Create a ***Script*** in ***ServerScriptService***.

2. Add the code below. You can change the effect to anything that you like

```Lua
-- Function to make a part glow
local function makeGlow(part)
    part.Material = Enum.Material.Neon
    part.BrickColor = BrickColor.new("Bright yellow") -- Change to your preferred glow color
end

-- Function to make a part stop glowing
local function stopGlow(part)
    part.Material = Enum.Material.Plastic
    part.BrickColor = BrickColor.new("Institutional white") -- Change to your preferred default color
end

-- Connect each part in the Workspace to the touch events
for _, part in pairs(workspace:GetChildren()) do
    if part:IsA("BasePart") then
        part.Touched:Connect(function(hit)
            makeGlow(part)
        end)
        part.TouchEnded:Connect(function(hit)
            stopGlow(part)
        end)
    end
end

```





