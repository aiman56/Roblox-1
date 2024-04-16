<link rel="stylesheet" type="text/css" href="styles.css" />

# Roblox  1 : Intro to Roblox <!-- omit from toc -->

<hr>

## Table of Contents <!-- omit from toc -->
- [Creating New Experience](#creating-new-experience)
- [Moving the Camera](#moving-the-camera)
- [Inserting Parts](#inserting-parts)
- [Selecting Parts](#selecting-parts)
- [Moving Parts](#moving-parts)
- [Scaling Parts](#scaling-parts)
- [Rotating Parts](#rotating-parts)
- [Customizing Colors and Materials](#customizing-colors-and-materials)
- [Anchoring Parts](#anchoring-parts)
- [Deleting the Baseplate](#deleting-the-baseplate)
- [Playtesting the Course](#playtesting-the-course)


This tutorial explains the basics of  [Roblox Studio](https://create.roblox.com/docs/studio/setting-up-roblox-studio)  by building, playtesting, and publishing a simple platformer experience. Follow each section and learn how to:

-   Create the foundation of your platformer using one of Studio's bundled templates.
    
-   Navigate around the 3D viewport to see the environment from every angle.
    
-   Create platforms for players to traverse using Studio's primary building blocks.
    
-   Playtest and troubleshoot your experience.
    
-   Make your experience available for everyone on Roblox to play.


## Creating New Experience

[Roblox Studio](https://create.roblox.com/docs/studio/setting-up-roblox-studio), a free application available on Windows and Mac, is the essential building tool for Roblox experiences.

With Studio open, create a new place by pressing  <kbd>Ctrl</kbd> + <kbd>N</kbd>. Alternatively, click the  Baseplate  template under the  All Templates  tab.

<p align="center">
    <img src="..\Assets\Baseplate-Template-Icon.png.webp" alt="drawing" width="200"/>
</p>

The Baseplate template consists of a spawn location where player characters appear in the world when they enter the experience, as well as a wide open baseplate floor.

<p align="center">
    <img  src="..\Assets\New-Template-With-Spawn-Location.jpg.webp"  alt="drawing2"  width="400"/>
</p>

## Moving the Camera

| Key                                                 | Action                                                        |
| --------------------------------------------------- | ------------------------------------------------------------- |
| <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> | Moves the camera forward, left, back, or right                |
| <kbd>Q</kbd> <kbd>E</kbd>                           | Moves the camera up or down                                   |
| <kbd>Shift</kbd>                                    | Increase the camera movement speed                            |
| <kbd>F</kbd>                                        | Focuses the camera on the specific part                       |
| <kbd>Right Mouse Button</kbd>                       | When pressed, dragging the mouse moves the camera view around |
| <kbd>Mouse Scroll Wheel</kbd>                       | Zooms the camera in or out                                    |
| <kbd>Middle Mouse Butto</kbd>                       | When pressed, dragging the mouse pans the camera              |

## Inserting Parts

A **Part** is Roblox's primary building block. You can **move**, **resize**, and **rotate** parts, as well as customize their appearance, such as their **color and material**. There are five different part types that you can insert through the Parts section of the **Home** or **Model** tabs

To insert a part :

1. In the menu bar, select **Model** tab.

<p align="center">
    <img  src="..\Assets\Toolbar-Model-Tab.png.webp"  alt="drawing3"  width="600"/>
</p>

2.  Under the  **Part**  button, click the dropdown arrow to reveal the  part type picker  and choose a part type.



<p align="center">
    <img  src="..\Assets\Model-Tab-Part-Type-Picker.png.webp"  alt="drawing4"  width="600"/>
</p>

3. Click the button to insert a part of the chosen type into the world.

<p align="center">
    <img  src="..\Assets\First-Inserted-Part.jpg.webp"  alt="drawing5"  width="600"/>
</p>


## Selecting Parts

Inserted parts are automatically selected, and you can select parts at any time with the **Select** tool. Hovering over and clicking a part selects it, and you can select multiple parts by holding <kbd>Shift</kbd>, <kbd>Ctrl</kbd> or <kbd>⌘</kbd> as you hover over and click them.

<p align="center">
    <img  src="..\Assets\Model-Tab-Select.png.webp"  alt="drawing6"  width="600"/>
</p>

## Moving Parts

1. With the newly inserted part selected in the 3D viewport, toggle on the **Move** tool.

<p align="center">
    <img  src="..\Assets\Model-Tab-Move.png"  alt="drawing7"  width="600"/>
</p>

2. Click and drag the arrow that's pointing in the direction you want to move the part. Remember that this is the first platform players will jump to, so you should move it just slightly away for an easy first jump.

<p align="center">
    <img  src="..\Assets\First-Part-Moved.jpg"  alt="drawing8"  width="600"/>
</p>

## Scaling Parts

Similar to **moving**, parts scale along the X, Y, and Z axes. You can make a part larger or smaller by using the Scale tool.

1. With the platform part still selected in the 3D viewport, toggle on the Scale tool.

<p align="center">
    <img  src="..\Assets\Model-Tab-Scale.png.webp"  alt="drawing9"  width="600"/>
</p>

2. Click and drag the handles to scale the part up in size, making the platform easier for players to land on from the first jump.

<p align="center">
    <img  src="..\Assets\First-Part-Scaled.jpg.webp"  alt="drawing10"  width="600"/>
</p>

## Rotating Parts

Similar to **moving** and **scaling**, parts rotate around the X, Y, and Z axes. By default, parts rotate incrementally by degrees.

1. With the platform part still selected in the 3D viewport, toggle on the Rotate tool.

<p align="center">
    <img  src="..\Assets\Model-Tab-Rotate.png.webp"  alt="drawing11"  width="600"/>
</p>

2. Click and drag a circle to rotate the part in that direction.

<p align="center">
    <img  src="..\Assets\First-Part-Rotated.jpg.webp"  alt="drawing12"  width="600"/>
</p>

## Customizing Colors and Materials

The fastest way to recolor a part is through the hexagonal color picker accessible through the small dropdown arrow under the **Color** button. By default, picking a color applies it to all selected parts. Alternatively, you can apply a chosen color as a painting tool by toggling on **Color Action as Tool** and clicking specific parts in the 3D viewport.


<p align="center">
    <img  src="..\Assets\Model-Tab-Color-Tools.png.webp"  alt="drawing13"  width="600"/>
</p>

<p align="center">
    <img  src="..\Assets\Hexagon-Color-Picker.png.webp"  alt="drawing14"  width="600"/>
</p>

You can also customize a part's material to simulate real-world materials such as wood, glass, or fabric. A part's material affects both its visual appearance and its physical traits; for example, the **Concrete** material is heavier than the **Plastic material**.

To apply different materials to parts:

1. Open the **Material Manager**.

2. In the **3D viewport**, select one or more parts.

3. In the **Material Manager** palette, hover your mouse over the desired material (you don't need to select it) and click the **Apply** to **Selected Parts** button.

<p align="center">
    <img  src="..\Assets\Apply-To-Selected-Parts.png.webp"  alt="drawing15"  width="600"/>
</p>

<p align="center">
    <img  src="..\Assets\First-Part-Styled.jpg.webp"  alt="drawing16"  width="600"/>
</p>

## Anchoring Parts

Since platforms should remain fixed in space, you'll need to anchor each part that you insert into the world.

1. In the **3D viewport**, select each of the platform parts you've inserted into the world.

2. Toggle on the **Anchor** option in the Parts section.

<p align="center">
    <img  src="..\Assets\Model-Tab-Anchor.png.webp"  alt="drawing17"  width="600"/>
</p>

## Deleting the Baseplate

To provide a consequence when players miss a jump, you can delete the baseplate, forcing them to restart from the spawn location each time.

1. Access the **Explorer** window. If it's not currently open, click **Explorer** from the **View** tab.

<p align="center">
    <img  src="..\Assets\View-Tab-Explorer.png.webp"  alt="drawing18"  width="600"/>
</p>

2. Expand the top-level **Workspace** tree, locate the **Baseplate** object, and select it.

<p align="center">
    <img  src="..\Assets\Workspace-Baseplate-Selected.png.webp"  alt="drawing19"  width="600"/>
</p>

3. Press <kbd>Delete</kbd>. The course now floats in an empty sky.

<p align="center">
    <img  src="..\Assets\Course-No-Baseplate.jpg.webp"  alt="drawing20"  width="600"/>
</p>

## Playtesting the Course

To playtest your experience, click the Play button in the menu bar.

<p align="center">
    <img  src="..\Assets\Model-Tab-Quick-Access-Play.png.webp"  alt="drawing21"  width="600"/>
</p>

While playtesting, you can use the same controls as a default Roblox experience:
<div align="center">

| Key                                                 | Action                                                        |
| --------------------------------------------------- | ------------------------------------------------------------- |
| <kbd>W</kbd> <kbd>A</kbd> <kbd>S</kbd> <kbd>D</kbd> | Moves the chararter forward, left, back, or right             |
| <kbd>Space</kbd>                                    | Jump                                                          |
| <kbd>Right Mouse Button</kbd>                       | When pressed, dragging the mouse moves the camera view around |
| <kbd>Mouse Scroll</kbd>                             | Change camera zoom                                            |

</div>


