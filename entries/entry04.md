# Entry 4
##### 3/16/23

### Context

With the exercise section of the routine page and the "pass day" system set up already by me and Ronnie, We are finally able to decide the inputs and stats for our game. Anson, who was responsible for the character sprites, had created the majority of the sprites needed to continue with our game. 

### Diet section

The first thing I did after completing the exercise section was the diet section on the opposite side of the journal. The diet section will have the same function as the exercise section so I basically took the same code and created one for the diets. In general, both exercise and diet will be able to input the choices on the bottom and place them in the display boxes. When the reset button is clicked, the boxes will empty. 

<img width="404" alt="image" src="https://user-images.githubusercontent.com/73482897/225748639-7a44f4a3-bcd5-4c73-828b-44d8979fa734.png">


### Create choices for exercises & diets

Since the routine page was functionally created, it is available to start creating the different choices for the player. For the exercise section, I created a `muscleMassIndex`, which is the indicator of weather or not the player muscle mass is going to increase that day. There are 3 different choices for exercise: cardio, dumbell exercise, intenses dumbell exercise (placeholder name). Each exercise have a different integer representing their contribution to the `muscleMassIndex`. For example, dumbell exercise will increase the `muscleMassIndex` by 2, meaning the next two days, the player will be able increase their muscle depending on their caloric intake. While intense dumbbell exercises have a contribution of 4 and cardio with -1. Each of these exercises of course burns a different amount of calories with cardio as the highest of them all. 

<img width="432" alt="image" src="https://user-images.githubusercontent.com/73482897/225748839-03aafd5a-f918-44d9-8da7-dc982d5ebf4a.png">

Diets are simpler to understand compared to the exercise section, Diets will only have a calorie section. Therefore, the three different diets are basically low, mid, high calories choices. 

### Stat choices

Me and my partners finalized on 5 stats total, them being:

* Weight
* Body fat
* Muscle Mass
* Determination
* Metabolism

Weight is going to be the most abstract stat that is usually the easiest to determine simply by a scale, so It is necessary to show this stat publicly on the journal stat page. The weight will include the muscle mass and body fat of the player. 

We use body fat and muscle mass to determine the different stages that people might have. There are three stages of body fat, low, mid and high and same goes with muscle mass. This means that there are 9 different sprites, representing the 3 stages of body fat and 3 stages of muscle mass. For example, low body fat and high muscle mass will be a different sprite compared to high body fat and low muscle mass. 

Determination, This stats will be the game's event trigger and possibly a lose condition. When a player pushes their character too much, the character will lose determination which is out of 100%. For every percent lost in the process of trying to achieve their goals, the more likely the character will go off the planned routine. For example, if the character has 60% determination, they will have a 40% chance of going off the planned diet or exercise on the plan page. When the player's determination drops to 0%, the player will always go off the plan and relapse, which would possibly be our lose condition. 

Metabolism: the character's caloric burn without doing anything. Meaning it is the calorie required just to live. This stat is going to be changing depending on the character's diet. If a player eats too little, their metabolism will drop to save energy. The opposite is true as well. 

<img width="351" alt="image" src="https://user-images.githubusercontent.com/73482897/225748919-c5065c4c-b0e2-4733-8d90-b3ba132c53b4.png">

### Stat changes by routine

As discussed above, the player's choices will have an impact towards their stats. Eating above the calories burned (metabolism + exercise burned < calories consumed) will make the character be at a caloric surplus. While being at a caloric surplus, the player's muscle will increase at a percentage of 75 for the first 500 calories that exceeds the calories burned. With 25 percent of them going to body fat. After exceeding the 500 calorie mark, the percentages of body fat and muscle increase with flip. Therefore the player would want to have a caloric surplus below 500 for clean bulking. While the player has their metabolism increase during this phase, not only because the body is getting more energy but also building muscle. 

If the player eats below the calories burned, the character will be at a state of caloric deficit. In this state, the character will lose fat at 75% and 25% of muscle for the first 500 calories below the calories, then after the 500 caloric deficit mark, the percentages of loss will flip. While the player has their metabolism decrease depending on the intensity of the deficit. 

However, you can still build muscle while not exercising, but just at a bad ratio. The extra calories will build at 80% fat and 20% muscle. 

* FYI - these changes in the stats do not cover all variables in the real world. Do not take these changes to your body too literally. 

<img width="301" alt="image" src="https://user-images.githubusercontent.com/73482897/225750230-f4a40822-a236-4309-964a-5f575ae544b9.png">

### Engineering Design Process

Currently me and my partners are still in the process of creating a minimum viable product / prototype as some of the features we wanted have yet to be implemented. The routine is THE most core function of the game but there are other features that would make this game so much more engaging. Therefore, we want to keep on building this prototype until the two other wanted features are implemented. 

### Skills 

In the process of creating stat changes, It is very important to keep attention to the details as to not create mistakes in this phase. Since there are a lot of modifications going on in the background, the mistakes can be easily hidden. By utilizing my attention to detail, I was able to prevent the mistake happening or will be able to figure out the mistake faster. Another skill I have implemented is logical reasoning. In this core phase of the game, many of the modifiers are researched from the internet, such as average weight, muscle / fat weight. Caloric surplus and deficit and its effects on the human body are all things that need to make sense when coding. Although the game is not able to cover all aspects of the body functions (micronutrients of diets), I would say that it stems from reality. 

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
