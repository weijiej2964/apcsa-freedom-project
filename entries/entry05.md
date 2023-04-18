# Entry 5
##### 3/18/23

### Context

After starting to create the algorthom for the character stat changes, the foundation for the game is basically done. However to push the game to its minimum viable product, there are still many places I need to polish. This blog is going to be the process of pushing my game to its MVP state. 

### Events

Events is the things that might happen to us on a daily basis. It could be because something out of our control or because of our own mindsets. These events could be both positive and negative. This is the other function I wanted to implement in my last blod entry.

To create the events for the game, I had to create two classes, the "RandomEvents" class and "TheEvents" class. Both classes serve a specfic purpose. The RandomEvent class sets the foundations for each event. Each event is going to change the character stat in some kind of way, while having a string as an explanation. It calls the player instance I had already created in `InitStat` so I could just call `changeStat` to change the stat based on the variables I set. 

The `TheEvent` class on the otherhand is the array that contains these events. Since I want to have different events to happen depending on the difficulty, I think the best way to do it is by seperating them by methods. The normal method in the `TheEvent` class is the method that adds the events into the array that would later be called. 

In `TheEvent` there are two different arrays, one is random and one is determination based. Random is self-explanatory, it is events that we as the player have no control over, such as a accident that might occur. While on the other hand, determination based is "bad" events that occur depending on how low the player's determination factor is. It generates a random number from 0 to 100 and compares it to the player's determination stat, if it is higher, it will trigger a determinationbased event, which means it is more likey to occir when we have a lower determination factor. 

There are two other methods, one to go and set a event as the occuring event that consider 

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
