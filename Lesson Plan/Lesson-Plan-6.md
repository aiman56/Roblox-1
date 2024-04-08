<link rel="stylesheet" type="text/css" href="styles.css" />

# Roblox  1 : Enviromental Building and Effect  <!-- omit from toc -->

<hr>    


## Table of Contents <!-- omit from toc -->
- [Environment in Roblox](#environment-in-roblox)


## Environment in Roblox

We have created our map, but do we make if feel real? Creating a virtual world is about more than just putting things in place—it's about making players feel like they're really there. That means paying attention to every little detail, from how the land looks to the sounds you hear. By focusing on making our map feel rich and believable, we can make it a place players will love to explore.

### Lighting

Let's start to add more enviromental details to our maps to make it feels and looks more realistic to the player. The first type of enviromental details that we want to add to our game is the ***Lighting***. We can control how the ***Lighting*** will affect our game by determining what time of the day it is,how strong the light is and the kind of shadow that it will produce when it hits and object.



1. To start, open the last project that you have created in ***Roblox Studio*** that contains the map layout that you have designed.
   
2. Make sure that the ***Explorer*** window is open on the left side of your screen. If it is not, you can refer to our past lesson on how to do so.
   
3. <kbd>Left Mouse Click</kbd> the ***+*** button on the left side of ***Workspace*** and add the ***Script***.

<p align="center">
    <img src="..\Assets\drawing61.png" alt="drawing61"  width="250" style="border: 2px solid  gray; margin-right: 60px;"/>
    <img src="..\Assets\drawing62.png" alt="drawing62"  width="250" style="border: 2px solid  gray;"/>
</p>


4. Open the ***Script*** and type the below. This allow us to access the ***Lighting*** service in the ***Script***.

```Lua
local Lighting = game:GetService("Lighting")
```

5. To change the time in the game, we need to create a variable of which we can use to set the time in the game.In Roblox, time is typically measured in minutes after midnight, where midnight is represented as 0 minutes. For example, if dusk is at 6:00 PM, which is 18 hours after midnight, you would calculate it as *18 hours * 60 minutes/hour = 1080 minutes*. To make it easy for you, you can just refer the table below to determine the value of the variable that need to be created.

<div class="table_component" role="region" tabindex="0" align="center">
<table>
    <thead>
        <tr>
            <th>Time</th>
            <th>Value</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>
                <div>
                    <div>5.00 AM&nbsp;</div>
                </div>
            </td>
            <td>300</td>
        </tr>
        <tr>
            <td>
                <div>7.00 AM&nbsp;</div>
            </td>
            <td>&nbsp;420</td>
        </tr>
        <tr>
            <td>12.00 PM</td>
            <td>720</td>
        </tr>
        <tr>
            <td>3.00 PM&nbsp;</td>
            <td>900</td>
        </tr>
        <tr>
            <td>&nbsp;6.00 PM</td>
            <td>1080&nbsp;</td>
        </tr>
        <tr>
            <td>9.00 PM</td>
            <td>1260&nbsp;</td>
        </tr>
        <tr>
            <td>12.00 PM&nbsp;</td>
            <td>0</td>
        </tr>
    </tbody>
</table>
</div>

6. Let set our game to night to see how the light will affect our game. What can you observe from the game surrounding? It the lighting has changed? How a about the Sun's position?
   
```Lua
local Lighting = game:GetService("Lighting")
local NIGHT = 1320 -- Night at 10:00 PM (22:00)

Lighting:SetMinutesAfterMidnight(NIGHT)
```

7. Now that we know how do update the in-game time, lets try to some real application to the game. Lets try to create a day and night cycle in game. The hours in game will update for every seconds in real life.

```Lua
local Lighting = game:GetService("Lighting")

local TIME_SPEED = 3600 -- 1 hour = 1 hour (real-time)
local START_TIME = 9 -- 9am in-game

local minutesAfterMidnight = START_TIME * 60
local waitTime = 1 -- Wait for 1 second between each update

while true do
    -- Update time based on real-time passing
    local secondsPassed = TIME_SPEED * waitTime
    minutesAfterMidnight = (minutesAfterMidnight + secondsPassed / 60) % 1440 -- Ensure time wraps around after 24 hours

    -- Set the new time
    Lighting:SetMinutesAfterMidnight(minutesAfterMidnight)

    -- Wait for 1 second before the next update
    wait(waitTime)
end

```

### Atmosphere


The ``Atmosphere`` object in Roblox creates realistic environments by controlling how sunlight scatters and affects light transmission through the air. It allows creators to adjust atmospheric effects like haze and glare, making it easy to design scenes with beautiful sunsets or foggy afternoons, adding to the immersive experience of the game.


To change how the atmosphere will affect the ``Lighting``, we can do it in two places , the first place is in ***Properties*** windows and the second place is within the  ***Script***. Lets do it in the ***Properties*** window first.

1. Go to the ***Explorer*** windows and click ***Lighting***. You should see ***Atmosphere*** under ***Lighting***. Double click ***Lighting*** until you see the ***Properties*** windows under the ***Explorer*** windows.

<p align="center">
    <img src="..\Assets\drawing63.png" alt="drawing63"  width="200" style="border: 2px solid  gray;"/>
</p>

2. In the ***Properties*** windows, you can see a lot of options that can be changed. Try to play around the options particularly the ```Density```, ```Haze```, ```Glare``` and ```Color```. Try to see how it will affect the lighting and surrounding

<p align="center">
    <img src="..\Assets\drawing63.png" alt="drawing63"  width="200" style="border: 2px solid  gray;"/>
</p>

3. Now lets try to edit the ```Atmosphere``` in the ***Script***. Add new ***Script*** in the workspace.

4. Change the properties of ```Atmosphere``` as below. You can see that by running the code that the ```Atmosphere``` will change according to the properties given. So, why need to do it ***Script*** when we can do it so much easier in ***Properties*** windows. The reason is changing it in ***Properties*** windows only will change it at the start of the game. So if you want to create atmospheric effect that keep changing throughout the game , you can only do it in ***Script***. 

``` Lua
local Lighting = game:GetService("Lighting")

local atmosphere = Lighting.Atmosphere

atmosphere.Haze = 5
atmosphere.Density = 0.5
atmosphere.Glare = 3
atmosphere.Color = Color3.fromRGB(87, 255, 205)
```





