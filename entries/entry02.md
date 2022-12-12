# Tool Tinkering
##### 12/12/2022

### Context

In the following weeks of tinkering with Unity, I have got a basic understanding of the functionality of the engine. I organized my goals for the project and focused on learning a few key features. For example, the main function of changing text using code so each passing day can result in a change in the player statics. Also opening and closing certain user interfaces that are going to play a role in opening and closing the player stat interface. In addition I learned button `onClick ` events so that the player can interact with the game. 

### Click Event

Clicking event is the main way the player is going to interact with the game's functions, such as transitions, opening panels, etc. Therefore it is the first feature I dug into. The video I watched was [Master Unity Button OnClick actions](https://www.youtube.com/watch?v=Ky-bzQFxV2U&t=522s&ab_channel=CocoCode) by Coco Code, which go through Button compoent's UI functionality. TextMeshPro Button UI is a pre-created object element with the `button` component and a text element inside the object. TextMeshPro button UI is extremely useful and provides the foundation of a button, so all I need to do is code the functionality script and attach it to the button's `button` component. The button component is the core of the learning button and inside the component there is a `on click()` section for click events.

<img width="406" alt="image" src="https://user-images.githubusercontent.com/73482897/207149598-80ce3f98-1133-4e30-b10f-86744e65010b.png">

This section allows a script input, which can manipulate a target object. In this case, since I'm just printing out a message, there is not a specific object in target, therefore I will attach the script to the button itself and the `on click()` section. The script I attached is as follows. 

<img width="254" alt="image" src="https://user-images.githubusercontent.com/73482897/207150280-bab1ae50-5db0-4850-a8ac-1038c95e75aa.png">

Then when I press the button, it will work properly:

<img width="467" alt="image" src="https://user-images.githubusercontent.com/73482897/207150422-581f4304-7230-4d24-9442-a00eec71e024.png">

### Opening Panel

I watched the [tutoral](https://www.youtube.com/watch?v=aN11LnlF89I&ab_channel=Chris%27Tutorials) to find out that Opening panel is a fairly easy concept as it just involves a unity function called `SetActive(boolean)` which turns an object active and inactive.  When an object is active, the user can see and interact with the interface, and vice versa for inactive states. To put into perspective, I create a GameObject variable to store the target object and use that variable to set inactive/active. 

<img width="221" alt="image" src="https://user-images.githubusercontent.com/73482897/207151429-a403f1dd-ed03-49a8-84a8-15f51f6a8d07.png">

Then I just have to go to unity and tell the script that the "GameObject" is the one that I dragged on there. 

<img width="425" alt="image" src="https://user-images.githubusercontent.com/73482897/207151676-7e06ae69-89c2-42a7-9417-da148ba18a44.png">

### Editing

Editing content of an object is similar to turning on or off, but instead it's a component "text". Similar I created a variable to get the target object, which in this case is the text. Then since the script is attached to the text itself, I don't need to tell the system about which I'm talking about. Next, since the component is a "text" component, I could use .text to signal that I'm changing the text part of the component instead of the entire component. 

<img width="288" alt="image" src="https://user-images.githubusercontent.com/73482897/207152907-6a532ca2-3d95-461c-a5c5-871f5f7c65d0.png">

Therefore the text would change to 5 instead of blank as default. 

### EDP 

I am currently on step 2 and 3 of the engineering design process, researching/learning the project and brainstorming solutions as well. In the next blog, I desire to be on step 4, planning the project out. 

### Skills 

The skills I used in the past few weeks are reading, googling, and learning. Which is all essential for understanding a concept. I had to use googling skills to find resources regarding the feature I am learning, then by reading and learning skills to intake the information and put them to test. 

### Winter Break

For winter break, I want to make unity shared among my partners so we can finally start working on the same files and start making basic features such as start button, open journal, etc. 


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
