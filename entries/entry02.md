# Tool Tinkering
##### 12/12/2022

### Context

In the following weeks of tinkering with Unity, I have got a basic understanding of the functionailty of the engine. I organized my goals for the project and focused on learning a few key features. For example, the main function of changing text using code so each passing day can result in a change in the player statics. Also opening and closing certain user interfaces that is going to play a role in opening and closing the player stat interface. In addition I learned button `onClick ` events so that the player can interact with the the game. 

### Click Event

Clicking event is the main way the player is going to interact with the game's functions, such as transitions, opening panels, etc. Therefore it is the first feature I dug into. The video I watched was [Master Unity Button OnClick actions](https://www.youtube.com/watch?v=Ky-bzQFxV2U&t=522s&ab_channel=CocoCode) by Coco Code, which go through Button compoent's UI functionality. TextMeshPro Button UI is a precreated object element with the `button` compoent and a text element inside the object. TextMeshPro button UI is extermely useful and provides the foudation of a button, so all I need to do is code the functionality script and attach to the button's `button` compoent. The button compoent is the core of learning button and inside the compoent there is a `on click()` section for click event.

<img width="406" alt="image" src="https://user-images.githubusercontent.com/73482897/207149598-80ce3f98-1133-4e30-b10f-86744e65010b.png">

This section allows a script input, which can manipulate a target object. In this case, since im just printing out a message, there is not a specfic object im targeting therefore I will attach the script to the button itself and the `on click()` section. The script I attached is as follows. 

<img width="254" alt="image" src="https://user-images.githubusercontent.com/73482897/207150280-bab1ae50-5db0-4850-a8ac-1038c95e75aa.png">

Then when I press the button, it will work properly:

<img width="467" alt="image" src="https://user-images.githubusercontent.com/73482897/207150422-581f4304-7230-4d24-9442-a00eec71e024.png">

### Opening Panel

Opening panel is a fairly easy concept as it just involves a unity function called `SetActive(boolean)` which turns a object active and unactive. When a object is object is active, user can see and interact with the interface, and vise versa for unactive state. To put into perspective, I create a GameObject variable to store the target object and use that variable to set unactive/active. 

<img width="221" alt="image" src="https://user-images.githubusercontent.com/73482897/207151429-a403f1dd-ed03-49a8-84a8-15f51f6a8d07.png">

Then I just have to go to unity and tell the script that the "GameObject" is the one that I dragged on there. 

<img width="425" alt="image" src="https://user-images.githubusercontent.com/73482897/207151676-7e06ae69-89c2-42a7-9417-da148ba18a44.png">

### Editing

Editing content of a object is similar to turning on or off, but instead its a compoent "text". Similar I created a variable to get the target object, which in this case is the text. Then since the script is attached to the text itself, I don't need to tell the system about which I'm talking about. Next, since the compoent is a "text" compoent, I could use .text to signal that I'm changing the text part of the compoent instead of the entire compoent. 

<img width="288" alt="image" src="https://user-images.githubusercontent.com/73482897/207152907-6a532ca2-3d95-461c-a5c5-871f5f7c65d0.png">

Therefore the text would change to 5 instead of blank as default. 

### EDP 

I am currently on step 2 and 3 of engineering design process, researching/learning the project and brainstorming solutions as well. 


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
