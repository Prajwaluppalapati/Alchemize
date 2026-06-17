# Getting Started with Unreal Engine
 
## Installation
 
Download the Epic Games Launcher from [unrealengine.com](https://www.unrealengine.com) and create a free Epic Games account. Once inside the launcher, go to the Unreal Engine tab, click Library, and click the + button to add the latest UE5 version. The download is roughly 25–35 GB.
 
## Creating Your First Project
 
1. Open the Epic Games Launcher and click **Launch**.
2. The Unreal Project Browser will open. Click on create project on the left.
3. The Unreal Project Browser will open. Choose a template (Blank, Third Person, First Person, etc).

![Project Defaults settings](ProjectTemplates.png)

3. Set your project to **Blueprint** (easier for beginners) or **C++**.
4. Choose a project name and folder.

![Project Defaults](ProjectDefaults.png)

5. Click **Create**.

## Getting started to getting started

Upon opening up your editor you will be greeted with something like this

![UnrealEngine]({53C07650-5B0A-4B85-B6BE-A06089B9268A}.png)

This is the open world map, this is simply too complex to work with, so to get started go to

File ----> **Create new level**

![Create new level]({61EAEA79-3C6E-4D72-BF51-D7EF79A313F8}.png)

Then click on basic and create

![alt text]({9CB48A3B-AC17-4F5E-A198-3FB030B92747}.png)

Then click on save or simply **CTRL + S**, save it in contents

![Save Map]({F10B5709-6881-4C79-8D32-FE2CE27D11C6}.png)

Then go to **edit** ---> **Project Settings** -------> **Maps and modes**

![Maps and modes]({D942C619-4F11-48B3-8296-76C5ED8153B4}.png)

Click on both **Editor Startup Map** and **Game Default Startup Map** and select your saved level

![Selecting New Map]({1A3B321A-BDDA-41C6-B8D8-34F5510D4384}.png)

What this essentially does is whenever you open your project again, it will always open up in this level as opposed to the default open world level. This is where we will learn the basics of Unreal Engine


## The Editor Interface
 
### Viewport

The 3D scene view. This is where you preview most of your stuff and build your level. To navigate around your 3D viewport, you can hold **Right Mouse Button** and move around using WASD using your mouse to look around. Alternately you can hold down the **Left Mouse Button** and move your mouse to move around but that is less accurate

![Moving Around Viewport](MovingAround.gif)

You can add either **basic objects** or from the **content drawer**(discuss later) and interact with them. 
When you click on an object, you can move it around, rotate it or scale it. These modes can be changed using **W, E, R** keys on the keyboard. 

- W key allows you to move an object
- E Key allows you to rotate them
- R key allows you to scale them

![Moving, Rotating and Scaling](MovingRotatingAndScaling.gif)

(Recording did not capture it but I went to **Get Content** --> **Shapes** --> **Cube**)

You can also duplicate objects by either using **CTRL+C** and **CTRL+V**
or you can **hold ALT while moving an object** to duplicate

![Moving, Rotating and Scaling](DuplicatingObjects.gif)

All level design is done in the viewport, it depends on how you wanna make your game.


### Outliner
The outliner is this tab over here, it lists all the characters in your current level
![Outliner]({521EDF2B-FADE-4F38-80ED-66FD5EAC50C5}.png)

It allows you to select your objects and view them in the details panel

### Note: My UE5 Layout might differ from yours, you can simply move windows around you by clicking on their tabs


### Details Panel
Located in the bottom right. Shows the selected Actor's properties — position, scale, materials, and more.
 
### Content Browser
Located at the bottom. Your project's library of assets: meshes, textures, sounds, and Blueprints.

