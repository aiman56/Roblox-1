# Roblox  1 : Lua Scripting Fundamentals <!-- omit from toc -->

<link rel="stylesheet" type="text/css" href="styles.css" />

<hr>    

## Table of Contents <!-- omit from toc -->
- [Creating a Script](#creating-a-script)
- [Testing Output](#testing-output)
- [Variables](#variables)
- [Object Properties](#object-properties)
- [Changing Part's Property](#changing-parts-property)
- [Parents and Children Relationship](#parents-and-children-relationship)
- [Creating a Function](#creating-a-function)

## Creating a Script

Scripts are commonly created in ServerScriptService, a special folder made just for holding scripts.

1. In Explorer, hover over ***ServerScriptService*** to see the ***+*** button.

<p align="center">
    <img src="..\Assets\hover-over-serverscriptservice_400x400.png.webp" alt="drawing21" width="400"/>
</p>

2. Click the ***+*** button and select ***Script***. A new script will be created and the script editor will open.

3. Right-click ***Script*** and select ***Rename***. Name the script ***PracticeScript***.

<div class="page"/>

## Testing Output

1. Select the ***View*** menu tab.

2. Click ***Output***.

<p align="center">
    <img src="..\Assets\enable-output-window_600x200.png.webp" alt="drawing22" width="600"/>
</p>

The window will appear at the bottom of Roblox Studio.

<p align="center">
    <img src="..\Assets\coding-1-output-window_800.png.webp" alt="drawing23" width="600"/>
</p>

3. To test the script, click ***Play***. `Hello world!` will show up in the Output window.

<p align="center">
    <img src="..\Assets\helloworld-output_800x150.png.webp" alt="drawing24" width="600"/>
</p>

4. Click Stop to end the playtest. You can now return to the Script tab.

## Variables


In Lua, to declare a new variable, type `local`, then type the name for the new variable. A variable that can hold a player name might look like: `local playerName`

New variables are empty. To assign it a value, or put something inside its container, use the `=` symbol. In this case, assign the variable the name of your favorite animal.

After the variable name, type `=` to assign the value to the variable.

```Lua
local myAnimal = "Tiger"
```

To print the variable, use the `print()` function
```Lua
local myAnimal = "Tiger"
print(myAnimal)
```

## Object Properties


The Properties window can be used to learn about an object's properties. Use it to take a look at a part's properties.

1.Select a part.

1. In the ***Properties*** Window on the bottom-right, look at the different properties that can be changed, like color, size, material and transparency. You can also change most properties in this window from within a script

<p align="center">
    <img src="..\Assets\part-properties_400.png.webp" alt="drawing25" width="400"/>
</p>


## Changing Part's Property


To make changes to a part, you must be able to describe the part's location. The ***Explorer*** is an excellent tool for referencing locations. In this case, ***PracticePart*** is under ***Workspace***.

<p align="center">
    <img src="..\Assets\practice-part_400.png.webp" alt="drawing26" width="400"/>
</p>

Now that you know where the part is, the part's location needs to be translated into something a script can understand.

1. Based on the picture, we can see that ***PracticePart*** is located under ***Workspace***. So, to do anything to affect the part, type `workspace.PracticePart`.
```Lua
workspace.PracticePart 
```

1. To change ***PracticePart***'s property, type `.Color` to access the ***Color*** property

```Lua
workspace.PracticePart.Color
```

3. For the part, the script will change its Color property to a new Color3, a data type that stores colors. Type `= Color3.fromRGB()` This code will allow you to assign a new color.

```Lua title="Test"
workspace.PracticePart.Color = Color3.fromRGB()
```

4. RGB color values can be manually typed inside the parentheses, but using the color picker is easier. Click inside the parentheses, and then click the color wheel. Follow the popup to create a color.

<p align="center">
    <img src="..\Assets\color-picker_800x140.png.webp" alt="drawing27" width="400"/>
</p>

<div class="page"/>

## Parents and Children Relationship

Instead of running scripts from ***ServerScriptService***, you may want to attach a script to the part. 

To do this, you must understand parent and child relationships.

Parents and children are ways to describe the hierarchy between different objects. Anytime you've added a new part to Workspace, Workspace has been the parent object, and the part became a child object. When you added a script to ***ServerScriptService***, ***ServerScriptService*** was the parent, and the script was a new child.

1. Create a new part and rename it. This lesson will use ColorPart.

2. Right-click the part and select ***Insert Object > New Script***. Rename the script ***ColorChanger***.

3. Copy and paste the code below into ColorChanger. This version of the code is the same that you used before. It assigns a specific part to a variable.

```Lua
local colorPart = workspace.ColorPart
colorPart.Color = Color3.fromRGB(50, 240, 255)
```

A parent is anything with objects, like scripts or parts, attached below it. Anything under the parent is its children. In the example below, ***ColorPart*** is the parent, and ***ColorChanger*** is the child.



<p align="center">
    <img src="..\Assets\color-changer_400x216.png.webp" alt="drawing28" width="400"/>
</p>

With the current script, you can only change the color of a single part named ***ColorPart***. To change any part's color, you can design the code to work on the script's parent object, whatever it happens to be named. The code script.Parent, will go up the hierarchy and find the object the script is attached to. To make use of this relationship, you can use change the previous code to the example below.

<div class="page"/>

```Lua
local colorPart = script.Parent
colorPart.Color = Color3.fromRGB(50, 240, 255)
```

## Creating a Function


1. Create a new script in ***ServerScriptService***.
  
2. Rename the script ***FunctionsPractice***.
  
3. Type local function `printFood()`, then press <kbd>Enter</kbd> on your keyboard. It should autocomplete the function to look like this

```Lua
local function printFood()

end
```

4. All of the code for your function has to be typed between the lines local function `printFood()` and `end`. Any code not between those two points won't run when the function does. For example like below 

```Lua
local function printFood()
  print("Pizza!")
end
```

5. Functions won't run until they are called. To call a function, type the function's name including the `()` at the end.

```Lua
local function printFood()
  print("Pizza!")
end
printFood()
```

6. Run the code as shown in the previous to see the output























