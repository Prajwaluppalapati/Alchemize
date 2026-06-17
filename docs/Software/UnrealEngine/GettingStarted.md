# Getting Started with Unreal Engine
 
## **Installation**
 
Download the Epic Games Launcher from [unrealengine.com](https://www.unrealengine.com) and create a free Epic Games account. Once inside the launcher, go to the Unreal Engine tab, click Library, and click the + button to add the latest UE5 version. The download is roughly 25–35 GB.
 
## **Creating Your First Project**
 
1. Open the Epic Games Launcher and click **Launch**.
2. The Unreal Project Browser will open. Click on create project on the left.
3. The Unreal Project Browser will open. Choose a template (Blank, Third Person, First Person, etc).

![Project Defaults settings](ProjectTemplates.png)

3. Set your project to **Blueprint** (easier for beginners) or **C++**.
4. Choose a project name and folder.

![Project Defaults](ProjectDefaults.png)

5. Click **Create**.

## **Getting started to getting started**

Upon opening up your editor you will be greeted with something like this

![UnrealEngine]({53C07650-5B0A-4B85-B6BE-A06089B9268A}.png)

This is the open world map, this is simply too complex to work with, so to get started go to

**File** ----> **Create new level**

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


## **The Editor Interface**
 
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

And once you are done playing just press **esc** on your keyboard to stop the session.


## **BluePrints**

In unreal engine there are mainly 2 types of Blueprints you work with, Level Blueprint and Blueprint Class

### **Level Blueprint**

**Level blueprint** is assigned to specific levels in a project. It controls the elements specific to that exact level.
So lets say for eg. you have multiple different levels, so you can control how each level would play out etc.

To open level blueprint you open the Blueprint Class window given in the photo,
then click on Level Blueprint

![BlueprintIcon]({3C44AD10-DEE8-4B57-A83F-42062986C948}.png)

### **A little extra setting**

if your window opens like this and you want it to open in the main window like your project settings

![BadWindow]({4D5C5E30-8F1C-4DA0-AEA3-07C753F2A62A}.png)

you can simply go to **Edit** --> **Editor Preferences** --> Search for **Asset Editor Location** and set it to **main window**

![Set Asset editor to main window]({BF455134-C07B-4F52-9428-3028DE8343F3}.png)

Now your window will open in a new window :D

so now your level blue print looks something like this

![LevelBlueprint]({3BF7E10A-FA4F-469F-B9D2-0734B7E066EE}.png)

You can zoom in and out using your **scroll wheel**
you can also move around by holding the **Right Mouse Button**.

Lets go over what each element is to understand it better

- **Event BeginPlay**: It is an event that fires everytime we begin play. It can be used in places like storing values for variables and stuff etc.

- **Event Tick**: It is an event that fires every tick or a set time between frames. This is used for repeatedly doing something every frame. You can get the time between frames by using **Delta Seconds**

- **Functions**: As the name suggests, they perform some instructions we give them. They may take input or give outputs. There are 2 types of functions, **pure** and **non-pure**. Pure functions are those which do not require execution pin (will discuss later) and non-pure require execution pins. Unreal has a bunch of inbuilt functions but we can create our own as well.

![Functions]({1DCC03F0-58C0-4C98-A489-EBE27523EE9B}.png)

- **Variables**: They are used to store items, they are in various data types like **int**, **bool**, **float**, **string** etc. and they can be of different types like **singe**, **array**, **set**, **map** etc. We can tweak their properties in the details panel

![Variables]({EF75FE68-B930-4FCA-BEBA-0313E8F3B9FE}.png)

There are a seperate type of variables called **Local Variables**, these exist only inside of functions and cannot be accessed outside.

That is all the basics of Level Blueprint, lets create a basic level blueprint to print a string.

First we need to drag off the **execution pin** on event begin play (Execution pin the small triangle at the end BeginPlay)
An execution pin is basically a pin that directs each event to fire. Its like a wire, when the we begin play, the wire is activated and all nodes connected to it also fire.

![BeginPlayExecutionPin]({D0A1A2D5-4B9E-4DF9-9887-F0C84C4BD6EE}.png)

After we drag of beginplay we can search for **Print String**, after selecting that we can hit enter
And then expand the drop down.

![BeginPlayExecutionPin](PrintString.gif)

Here we can see a bunch of settings, for now we will only focus on these ones:
- **In String**: This contains the thing you wanna print, for now I will leave that at Hello
- **Print to Screen**: Make sures that we want to print this to our screen or not
- **Text Colour**: Colour of the text we print
- **Duration**: How long we want it to stay on the screen (In seconds)

![PrintSettings]({182D206A-08BC-4549-AEB3-4E6E8A4EE197}.png)

These are my settings, you can copy them if you want or tweak and have fun yourself
After that lets hit play
And as you can see on the top left we have our message

![PlayMessage]({98284AB7-DCAC-4134-A17D-D499EF80D7F5}.png)

Now we can also add a **delay node**, so we can stop our game by using **esc**.
Go back to level blueprint

We can detatch nodes by 2 ways,

1) We can hold **ALT** and **left mouse click** on the execution pin

![RemovePin](RemovePin.gif)

2) Or we can hold **CTRL** and **click and drag** it around and **release** it on the pin we want to add it on

![RemovePin](ChangeExecPin.gif)

Do whatever feels best to you and add the delay nodes the same way we added our print node and join it to our print string
It should look like this

![DelayNodeAddedPrint]({777987C8-297C-45B6-B5AA-D2DB0AE06475}.png)

If you press play again, you will see the print string after the duration you set


Similarly if you hooked print string into **Event Tick**
you will see MULTIPLE print strings that spawn every frame

![PrintStringEventTick]({56AC35EA-E492-4A2D-B07F-614326B59ABE}.png)
![EventTickPrint]({A5DFBEF9-12F6-4057-B6BD-7E5E13D61306}.png)

For this guide I will only go over level blueprints as Blueprint classes are a little more complex and we will build in a more structured guide


## **Some Extra Stuff**


### **Compiling Blueprints**:

You should compile your blueprint after doing something big to check if everything works, you can compile by clicking the compile button on the top left

![CompileButton]({AC095D11-8D86-494F-A85A-DC0471B5B078}.png)

This ensures that no errors are present in case you create systems that are dependent on the current system.

### **Saving project**:

You can save the current object your editing by using **CTRL + S**

or you can save the entire project if there are any unsaved Changes using **CTRL + SHIFT + S**

### **Adding blueprints in between**

You can also add blueprints in between two blueprints by **right clicking** on the execution wire

![AddingBluePrintInBetween](AddingBlueprintsToExec.gif)

## **Wrapping Up**

That is all for this guide for now
I just wanted to give you a little taste of Unreal Engine.

It is a very powerful engine where you can create games by using just its visual scripting.
If you wanna learn more you can check out our other guides on this where I go deeper into how this engine works by creating hands on projects

Or there are plenty resources online

Till then have a fantastic day

![AddingBluePrintInBetween](Magic.gif)