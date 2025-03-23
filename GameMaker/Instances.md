### Instances in GameMaker

In GameMaker Studio 2, instances refer to individual objects that are placed into a room during gameplay. Each instance represents an active copy of an object in the game world at any given time. Objects define properties and behaviors (through code), but they do not exist in the game until an instance is created from them.

For example, if you have an object named `obj_Player` that defines how a player character should behave, such as moving left or right, jumping, etc., then each player-controlled character in your game will be an instance of `obj_Player`. You can create multiple instances of the same object in different rooms or at different times during gameplay.

Here’s a simple example using GML (GameMaker Language) to demonstrate creating and manipulating instances:

1. **Creating Instances:**
   ```gml
   // Create an instance of obj_Enemy at position (200, 300) in the room.
   instance_create_layer(200, 300, "Instances", obj_Enemy);
   ```

2. **Destroying Instances:**
   ```gml
   // Destroy all instances of obj_Enemy in the room.
   with (obj_Enemy)
   {
       instance_destroy();
   }
   ```

3. **Changing Instance Properties:**
   ```gml
   // Find an instance of obj_Player and change its speed to 5.
   var player = instance_find(obj_Player);
   if (player != noone)
   {
       player.speed = 5;
   }
   ```

Instances are fundamental in GameMaker because they allow you to create dynamic and interactive game environments, where objects can spawn, interact, and be destroyed as the game progresses.

#Instances #GameMaker