# Entry 5
##### 3/18/23

### Context

After starting to create the algorithm for the character stat changes, the foundation for the game is basically done. However, to push the game to its minimum viable product, there are still many places I need to polish. This blog is going to be the process of pushing my game to its MVP state. 

### Events

Events are the things that might happen to us on a daily basis. It could be because something out of our control or because of our own mindsets. These events could be both positive and negative. This is the other function I wanted to implement in my last blog entry.

To create the events for the game, I had to create two classes, the "RandomEvents" class and "TheEvents'' class. Both classes serve a specific purpose. The RandomEvent class sets the foundations for each event. Each event is going to change the character stat in some kind of way, while having a string as an explanation. It calls the player instance I had already created in `InitStat` so I could just call `changeStat` to change the stat based on the variables I set. 

```java
//create variables for the changes to each stat
  double weight, bodyfat, musclemass;
    int metabolism, determination;
    string text;
    Player player = InitStat.getPlayer();

    //create a constructor
    public RandomEvents(double w, double fat, double muscle, int deter, int meta, string text)
    {
        ...
    }

    public void changeStat()
    {
        player.setValues(weight, musclemass, bodyfat, determination, metabolism);
    }

```

The `TheEvent` class on the other hand is the array that contains these events. Since I want different events to happen depending on the difficulty, I think the best way to do it is by separating them by methods. The normal method in the `TheEvent` class is the method that adds the events into the array that would later be called. 

In `TheEvent` there are two different arrays, one is random and one is determination based. Random is self-explanatory, it is events that the player has no control over, such as an accident that might occur. While on the other hand, determination based is "bad" events that occur depending on how low the player's determination factor is. It generates a random number from 0 to 100 and compares it to the player's determination stat, if it is higher, it will trigger a determination based event, which means it is more likely to occur when the player has a low determination factor. 

``java
    static List<RandomEvents> RandomEvents = new List<RandomEvents>();
    static List<RandomEvents> DeterminationBasedEvents = new List<RandomEvents>();
    static RandomEvents CurrentEvent;
    static Player player = InitStat.getPlayer();

    public TheEvents()
    {
        
    }

    public static void Normal()
    {
        ...
    }

    public static void getRandomEvent()
    {
        if (Random.Range(0, 100) > player.getDetermination())
        {
            CurrentEvent = DeterminationBasedEvents[Random.Range(0, DeterminationBasedEvents.Count)];
        }
        else
        {
            CurrentEvent = RandomEvents[Random.Range(0, RandomEvents.Count)];
        }
    }
```

There are two other methods, one to set an event as the occuring event that considers determination when it randomly chooses an event. 

### Change Character Sprite

To change character sprites, I wanted to have 9 different sprites taken from the location of input. In `InitStat`, the place I first created our player, I added public sprite variables so I can just drag and drop the sprites into the desired places. After the sprite variables are added into the `InitStat` script, I just change the `Player` constructor to take in the sprites so each player instance has their own sets of sprites. 

```java 
 public Sprite ll, lm, lh, ml, mm, mh, hl, hm, hh;

    public Player(double w, double mass, double b, int d, double m, Sprite ll, Sprite lm, Sprite lh, Sprite ml, Sprite mm, Sprite mh, Sprite hl, Sprite hm, Sprite hh)
    {
        ...

        this.ll = ll;
        this.lm = lm;
        this.lh = lh;
        this.ml = ml;
        this.mm = mm;
        this.mh = mh;
        this.hl = hl;
        this.hm = hm;
        this.hh = hh;
    }
```
After I completed the setup, all I have to do is change the character sprites depending on the stats. The easy way to do it is just to create multiple conditionals that check the fat and muscle value then return the corresponding sprite. 

``` java 
public Sprite getCurrentPlayerBody()
    {
        if (bodyFat < weight*.08)
        {
            if (muscleMass < weight * .33)
            {
                return ll;
            }else if(muscleMass < weight * .39)
            {
                return lm;
            } else
            {
                return lh;
            }
        }
        else if (bodyFat <= weight * .19)
        {
            if (muscleMass < weight * .33)
            {
                return ml;
            }
            else if (muscleMass < weight * .39)
            {
                return mm;
            }
            else
            {
                return mh;
            }
        }
        else if (bodyFat > weight * .19)
        {
            if (muscleMass < weight * .33)
            {
                return hl;
            }
            else if (muscleMass < weight * .39)
            {
                return hm;
            }
            else
            {
                return hh;
            }
        }
        return ll;
    }

```
Then all I have to do to change the sprite is call this method above everytime I press the next day. 

### Change day to week

While I was recording the video, I realized that the game progresses very slowly because it was suppose to be a reflection of a more realistic situation. By the end of one of my playthroughs, I reached around 600 days before I reached the best physique in the game. Which, in a realistic standout, is a relevant choice however pressing the next day button 600 + times starts to seem repetitive. Therefore, I changed the stat changes so it is 10 times faster to gain and lose (10x because it is easier to just remove a 0 from the end). However, I still wanted to reflect a realistic stand point, so I decided to change the days to say weeks so it would make more sense. 
After changing this, I was able to keep the playthrough to less than 80 weeks. 

### EDP

I am on the Engineering Design Process step to test and improve. After this change to the game, It is at its minimum viable product. Therefore, most of what I did was to test and edit, such as changing the days to weeks. There are other errors I fixed along the way, but they are too minimal to be relevant in this blog entry. However, There is still one issue regarding mood and events, which is that I only added negative events as placeholders. This requires changes because over 60+ weeks the player who experiences 60+ negative events will easily lose due to uncontrollable factors. So to fix it, we still need to add positive events to balance the game out. 

### Skills

As I was pushing the project to completion, I used two skills the most. I had to use my debugging skills and attention to detail to find bugs and debug them. Since when I filmed the recording, I encountered many things I overlooked before. By doing multiple playthroughs, I was able to fix the game so it is more enjoyable. I would record the videos and if I see any details of errors, I would just simply fix it and try again. 




[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
