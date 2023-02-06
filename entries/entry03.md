# Entry 3
##### 2/6/23

### Context

After getting the journal to open, I have decided to add some art into the game along the way. As me and my partners do not have artistic foundations, we are going to build our game using pixel arts. Pixels require less details and are the easiest to create, as creating pictures for game objects could take a long time. Since player stat isn't completely decided between me and my partners, we decided to create the functions first and choose the stat/variables on that foundation. 

### Design 
To make sure our user interface is what we expected, we decided to add a simple prototype design to it to simulate the end result. By using [pixelartmaker.com](pixelartmaker.com), I was able to create the designs for the UI and some icons as well. 

<img width="474" alt="image" src="https://user-images.githubusercontent.com/73482897/217062797-401a1f0a-6d81-41ef-b630-bfddf037f87b.png">

As I was creating these designs, I realized that adding them in is also extremely easy. All I had to do was drag and drop the image into a folder in Unity, then drag the image as a "sprite" into the source image of the Image component of the game object. 

<img width="863" alt="image" src="https://user-images.githubusercontent.com/73482897/217063456-4f146293-194c-4fb5-ba1e-72b737981bf7.png">

After creating and adding them to the game objects, I was able to get the game to look much neater:

Home Page:

<img width="530" alt="image" src="https://user-images.githubusercontent.com/73482897/217063673-6e54cf36-4809-4761-b6f1-99ce0a90e1db.png">

Stats Page:

<img width="542" alt="image" src="https://user-images.githubusercontent.com/73482897/217063731-56d5a824-1ed5-45f0-a73a-c36b30be3ee8.png">

Routine Page:

<img width="547" alt="image" src="https://user-images.githubusercontent.com/73482897/217063785-219314f7-2fe9-443a-a791-927ab9de271b.png">

### Switching between pages

To different pages in the journal, I decided to separate the content of each page into groups. Then using the functions of a button, to set different pages to on/off to simulate a change of pages.

<img width="247" alt="image" src="https://user-images.githubusercontent.com/73482897/217064540-55b0dee5-2095-4eef-b4b9-5cf4cbc6dd17.png">

### Adding task to routine

As we all know, fitness is usually simplified to "move more, eat less". Although it is not completely correct, it has some facts to it. Therefore, I need to create a routine page, where the player is going to decide their actions of the day. I have come up with 3 exercises/diets a day to keep it simple. At first I struggled with this because changing the image and sprite of a game object is very different. To change how a game object looked, I needed to change the image.sprite instead of image. Knowing this, I create a list for exercise, where it's going to have its values and sprite stored. To understand how to create a list, I watched a [tutorial on the inventory system](https://www.youtube.com/watch?v=AoD_F1fSFFg&t=90s&ab_channel=SoloGameDev). 

<img width="410" alt="image" src="https://user-images.githubusercontent.com/73482897/217066233-ddf91286-cf76-4555-9a1a-72c6fd055af4.png">

Then once this method is created, we can create an object similar to how we create a folder. Once this is created, we can input our values and sprites into this instance. 

<img width="433" alt="image" src="https://user-images.githubusercontent.com/73482897/217066593-ae88a276-696e-45c1-b685-a4add971bad8.png">

Then I added this instance to the button where clicked, is going to add "cardio" to the daily plan. The addition is going to add a new instance to the list in planmanager. Then I created a loop to loop through all the instances in the list, taking their sprite element and changing the icons in the plan. 

<img width="532" alt="image" src="https://user-images.githubusercontent.com/73482897/217067493-6886d880-7abf-4972-84b0-5ffb8f9c3c0e.png">

### Removing task from routine

To remove the tasks from routine, I decided on a reset button as it is the easiest to implement and would cause a big inconvenience. To create this, all i have to make a button and make it run the code below to reset the list

<img width="378" alt="image" src="https://user-images.githubusercontent.com/73482897/217068085-13f43281-d407-4185-93f6-f5195b8f228d.png">

This code loops through the list and removes every instance in it, then sets the icon back to the default icon. 

### Engineering design process

I am currently in the engineering design process 4 & 5, planning and creating a prototype. Since our picture of the game is very abstract as for now, we have to create and plan along the way. With the routine function as the core of the game, after we create it, our progress will skyrocket. This is because of how the function links to different stats, mood, and events of the game. We will continue to create a prototype of this game, but we will be able to create stats and changes to the stats now we have the core almost done. 



### Skills

In the process of creating the game, two skills are used a lot. One of them is problem decomposition. Since our game is constructed of many major functions and seems very complex, breaking the functions into small tasks like switching pages, opening a journal, etc. Another skill I have used was "how to learn". At first failing to get the list to work, I tried to search up how to create this kind of system. I didn't even know what it is called so it was extremely hard to find. However, using this skill, I was able to understand the core foundation, and realized that it is like an inventory. Following the inventory I was able to get the list to work and finishing the rest is just basic work. 


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
