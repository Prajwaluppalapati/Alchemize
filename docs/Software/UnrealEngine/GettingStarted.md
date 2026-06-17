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
 
### **Viewport**

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


### **Outliner**

The outliner is this tab over here, it lists all the characters in your current level
![Outliner]({521EDF2B-FADE-4F38-80ED-66FD5EAC50C5}.png)

It allows you to select your objects and view them in the details panel

### Note: My UE5 Layout might differ from yours, you can simply move windows around you by clicking on their tabs
![Outliner](WindowDocking.gif)

### **Details Panel**

The details panel is an important window, 
It is where we can view and change the properties of an object like size, location, rotation
Shape, texture and any other properties we may link

![Outliner](DetailsPanel.gif)




### **Content Browser**

Everything we create or use in our project goes to content browser, everything from textures, to models to blueprints all sits there.

It is located on the bottom left

![ContentBrowserButton']({6C2351B8-74B6-4245-BB68-501056057A75}.png)

![ContentBrowser]({3B61479B-238D-46FD-A2A8-4398556B5286}.png)

You can create new items by **right clicking** and choosing whatever you wanna make.
It is often recommended to **clean up your content drawer** so its easy to move around content drawers. 

![ContentBrowser](ContentDrawer.gif)

You can also view and check out engine content but it is generally recommended not to mess around with it without a good knowledge of how the engine works

you can do so by clicking the **gear icon** on the top right of the content drawer and check **engine content**.

![EngineContentEnable]({E8DCED19-855F-4F34-BE55-F4D05F9DE850}.png)

you can go uncheck it if you don't wanna see it in your content drawer. 

### **Play in editor**

To play your game in editor you click the **green icon** at the top or press **Alt + P**

![PlayIcon]({1554BA11-88A9-4FBA-AF8B-01E2E081C9F7}.png)

While playing to break out you can press **Shift + F1** to break your cursor in editor
Since we dont have a character, we possess a default pawn 

To break out of the play through and view your level we can click the detach icon
it allows us to view our own character and the level. 

![Detach]({FA54DD72-87FC-46E5-828C-CB607B675B22}.png)

You can also simulate the level by using the simulate button

![SimulateButton]({21DD9D98-AFF5-485B-A6DC-FE669372A3D5}.png)

(This gif below shows the entire playthrough session and how it works)

![SimulateButton](PlayTest.gif)

As of now this all the basics we need to know to get started with unreal engine.