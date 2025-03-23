### Understanding Variables in GameMaker

In GameMaker Studio 2 (GMS2), variables are used to store data that can be manipulated during game execution. They act as containers for holding values such as numbers, strings, or even complex data structures like arrays and objects.

Variables can be defined at different scopes, which determines where they can be accessed in your code:

1. **Local Variables**: These exist only within the function or script they are declared in. For example:
   ```gml
   // This is a local variable inside a create event
   var health = 100;
   ```

2. **Instance Variables**: These are tied to a specific instance of an object and can be accessed from within that instance's code. For example:
   ```gml
   // Set an instance variable in the create event
   health = 100;

   // Modify the instance variable in another event
   health -= 10;
   ```

3. **Global Variables**: These are accessible throughout the entire game from any object or script, making them useful for storing game-wide data like score, lives, etc.
   ```gml
   // Set a global variable in the start of the game
   global.score = 0;

   // Increment the global variable elsewhere
   global.score += 10;
   ```

4. **Static Variables**: These are similar to instance variables but they retain their value across instances of the same object type. They can be useful for maintaining state information that should persist between different instances.
   ```gml
   /// @description Increases the total number of enemies created
   static var enemy_count = 0;
   enemy_count++;
   ```

### Example Usage

Let’s create a simple example where we use a local variable to control an object's movement and a global variable to keep track of the player's score.

```gml
// Create Event of Object Player
global.score = 0; // Initialize the global score in the first frame if not already done
var speed = 5;    // Local variable for player speed

// Step Event of Object Player
if (keyboard_check(vk_right))
{
    x += speed;
}
else if (keyboard_check(vk_left))
{
    x -= speed;
}

if (place_meeting(x, y, obj_Enemy)) // Assume there is an enemy object called obj_Enemy
{
    global.score++; // Increase the score when player collides with an enemy
}
```

In this example:
- `speed` is a local variable that determines how fast the player moves. It exists only within the scope of the Player object's events.
- `global.score` is used to keep track of the player’s score, which can be accessed and modified from any other object or script in the game.

#Variables #GamaMaker