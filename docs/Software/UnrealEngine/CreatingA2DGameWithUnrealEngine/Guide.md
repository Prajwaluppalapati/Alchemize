# Creating a 2D Platformer using Unreal Engine

## **Some prerequisites**

It is recommended you go throught getting started with unreal engine guide before doing this guide.

### **Paper ZD**

Open your epic game's launcher and head on over to Fab, which is the fourth option on the side bar 

![FabImage](Images/FabShowcase.png)

Then search for **Paper ZD** and open it up
and then click on **add to library** 
After that click on install plugin, select the engine version you are working with and that should be first thing done.

![FabImage](Gifs/PaperZDInstall.gif)

### **Installing Plugins**

Create a new project, tweak your settings as you like

Then follow the following steps to enable these two plugins,

Click on **Edit** --> **Search Paper**, and then enable **Paper2D** and **PaperZD**
Then restart the engine

![EnablePaperZD](Gifs/PaperZDEnable.gif)

### **Recording Time**

All time recorded for unreal engine blueprints or the engine itself is to be done by using **Lapse** since unreal engine does not have native hackatime support.

You can **sync time** to **hackatime** through lapse

Check out: lapse.hackclub.com



## Getting 2D assets

A 2D game needs 2D assets, and dont we all LOVE free 2D assets.
The best website to get them are itch.io

You can click the link:
[Free 2D assets](https://itch.io/game-assets/free/tag-2d)

Although i used the following assets if you wish to follow along 1:1 with me

- **Tileset**: https://incolgames.itch.io/dungeon-platformer-tile-set-pixel-art
- **Character**: https://legnops.itch.io/red-hood-character

They are all completely free to download and play around with.


## Setting Up the Project

Although unreal engine does have a 2D template, we will learn from scratch by using an empty project.

First we will create a new map, set it as the default map for playing and opening levels. We have already discussed how to do this in the getting started guide. You can always refer back to it if you don't understand anything

Then we want to set up our project folder in the following way for ease of use

![FolderLayout](Images/FolderLayout.png)

Here, 
- **Assets**: This contains all our textures, models, sprites etc.
- **Blueprints**: This contains all the blueprints you will code
- **Maps**: Self explanatory, All the maps you create will go here


## Creating Redhood

Both the RedHood Character and the dungeon level are in sprite sheets. We will discuss how to use both of them in this section

But first we have to import them and prepare them.

### **Importing and Preparing Sprites**

In the itch.io section after clicking on download, we will proceed to downloads and install the **Idle and Alter.zip** file

![RedHoodInstall](Images/RedHoodInstall.png)

Then we will create a folder called RedHood in assets inside our project

We will extract the **Idle and Alter.zip** that and import them by opening the Content Drawer and clicking on **import**

![ImportRedHood](Gifs/ImportRedHood.gif)

If we open any one them, we can see its pretty blurry. There's an easy way to fix that
We can just go to the **details panel** on the right

Look under **Level of Detail**

Go to **texture group** and search for **"2D Pixels (Unfiltered)"**

![ChangingTextureGroup](Images/ChangingTextureGroup.png)

This would instantly improve the blurriness of the texture
**Press CTRL + S to save your progress**

Now to perform this action in bulk, we can select multiple texture groups by **holding SHIFT** and selecting using **Left Mouse Button**

Then Right Clicking, Going to **Asset Actions** --> **Edit Selection in Property Matrix**

![ChangingTextureGroup](Gifs/BulkEditInPropertyMatrix.gif)

First select all the items by either selecting them by **holding shift** or pressing **CTRL + A**

Here, expand the Level of Detail drop down and change texture group from **World** to **2D Pixels** then press **CTRL + A**

![ChangeCompressionSettings](Images/ChangeCompressionSettings.png)

Next up what we wanna do is extract these Sheets to sprites.

Before doing that we will clean up our folder structure a little better again.

Now under RedHood we will divide the folders into 5 parts, **Idle**, **Jump**, **Run**

Here each folder represents a seperate tilemap, since we wont be covering combat in this, you can go and delete **hurt** and **light atk** if you want

![RedHoodFolderStructure](Images/FolderStructure.png)

Then we can go ahead, click and drop each Texture map into its respective folder as follows

![RedHoodFolderStructure](Gifs/ShiftingToFolders.gif)

Now we can convert each of these into a sprite, this is done by right clicking a texture file, going under **sprite actions** and clicking on **extract sprites**

![Extract Sprites](Images/ExtractSprites.png)

Now a window like this should pop up

![ExtractSprites](Images/ExtractSprites1.png)

We do not want it to auto extract sprites for us because we want each sprite to be roughly the same size, to fix that you wanna go under **Sprite Extract mode** and select **Grid**

Now a seperate dropdown by the name of **Grid** should come up. 

Here we have to tweak the cell height and width. 
An easy way to get that is:

- To get cell width, count the number of items in a row and then divide it by the default length
- To get cell height divide, count the number of rows and divide it by the default height

You dont have to use a calculator, you can simply go to Cell Width enter box and just add a /(number of items you counted) infront of it

and then click extract

For eg. this is how I did it for the idle animation sheet.

![ChangeWidthLength](Gifs/ChangeWidthLength.gif)

By doing this we convert a sprite sheet into individual sprites, where each sprite is a frame in the animation

![RedHoodSprites](Images/RedHoodSprites.png)
 
We want to go ahead and do this with the rest of the sprite sheets we have until we have sprites for all 3 states.

### Incase your are unable to figure out

- For idle sprite sheet, divide the width by 18
- For jump sprite sheet, divide the width by 19
- For running sprite sheet, divide the width by 24

Click on extract and lets now convert them to animations

### **Creating FlipBooks**

In Unreal Engine, a flipbook is a 2D sprite animation asset, part of the **Paper2D** plugin. It works basically like a digital flipbook/sprite sheet animation.

a sequence of sprite frames played in order to create the illusion of motion, similar to how 2D games handle animation

Before doing that let us clean up our folders structure a little as well. Open up the content **Browser** and open the **redhood** folder

Inside of **Redhood** create two folders, one called **Sprites** and the other called **FlipBooks**

![FolderStrucForRedHood](Images/FolderStruc.png)

The shift the **Idle**, **Jump** and **Run** folder inside of sprites

![CleaningFolders](Gifs/CleaningFolders.gif)


To create flipbooks let us start by going into the sprites folder and let us start with idle animation

Select all the sprites beside sprite sheet

**Right click** and select **create flipbook**

You will get a flipbook with an option to rename it. You can keep whatever you want it's name to be

Generally I prefix flipbook with **FB_**, so I named it as **FB_Idle**

(In the GIF I accidentally renamed it as running, it is the idle animation)

### In Unreal engine we generally prefix assets with a letter or two to know better what kind of asset we are using, it also makes it easier to search

![CreatingFlipbook](Gifs/CreatingFB_Idle.gif)

We can then drag and drop this over to our **Flipbooks folder**


Similarly we can do the exact same process with run

Go over to **run folder**, select all sprites besides sprite sheet

right click, **create flipbook**

rename it to **FB_Run**, and then move it over to the **flipbooks** folder

If the animation feels slow, dont worry about it we will fix it soon

This is what your Flipbooks folder should look like now

![FlipBooks](Images/FlipbooksFolder.png)

Now let us create jump animation, jump animation works a little differently.
Even tho you can do the same thing, we want to divide our jump animation into 3 seperate parts

- **Jump start**: Plays at the start of jump
- **Jump loop**: Plays while in the air
- **Jump end**: Plays when a player lands

To do this, we will first create a normal Flipbook, and open it up

![FlipBookEditor](Images/FlipBookEditor.png)

This is what a flipbook editor looks like.

here you can control how fast the animation goes, key frames, default material etc.

We will not discuss this right now but rather focus on how can we divide these animations

At the bottom we have the the **animation player**, there we can adjust the player and make out where each animation starts.

You can play around with your choice but here is what came out for me after messing around with the anim player

- **Jump Start**: Jump starts from frame 0 - 3
- **Jump Loop**: Remains from frames 4 - 14
- **Jump End**: Remains from 15 to 18

Now we will go back to our sprites player, and select frames 0 - 3

![SelectFrames0and3](Images/JumpStartFrames.png)

**Right Click** --> **Create FlipBook**

name it to **FB_JumpStart**

Similarly we will select frames 4 - 14

Create flipbook, rename it to **FB_JumpLoop**

and finally select frames 15 - 18

Create flipbook, rename it to **FB_JumpEnd**

Then you can delete the entire jump flipbook and migrate the three flipbooks over to the Flipbooks folder

![FlipBooksRedHoodFolder](Images/RedHoodFlipbooksFolder.png)

## Creating BP_RedHood

For creating a working playable character we will now jump over to BluePrints

Blueprints is unreal engine's own visual scripting language that allows you to do a lot of things
We discussed a little bit of Blueprints in the Getting Started with unreal engine guide but we will put it to real use over here