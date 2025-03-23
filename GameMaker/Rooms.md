### Rooms in GameMaker

In GameMaker Studio 2 (GMS2), rooms are used to organize different scenes or areas within your game. A room can be thought of as a container that holds instances of objects, backgrounds, tiles, and other elements necessary to create a specific part of the game world. Each room can have its own unique setup, including background images, lighting conditions, views (camera settings), persistent objects, and entry conditions.

Rooms are essential for defining where and how different parts of your game will look and function. For example, you might have separate rooms for the main menu, gameplay levels, boss fights, or cutscenes. Each room can be designed independently, allowing for a modular approach to game development.

#### Example in GML

Here’s a simple example of how you might use rooms in GameMaker with GML (GameMaker Language):

1. **Creating a Room:**
   - In the GameMaker Studio 2 IDE, create a new room by right-clicking on the "Rooms" folder and selecting "Create."

2. **Adding an Object to the Room:**
   - Create an object that you want to place in your room. For example, let’s say we have an object called `obj_Player`.
   - In the room editor, click on the “Instances” tab and then click on the `obj_Player` icon from the objects list.
   - Click anywhere in the room view area to place an instance of `obj_Player` at that position.

3. **Using Code to Switch Rooms:**
   - You can use GML code to switch between rooms based on certain conditions, such as when a player reaches a specific point or completes a level.
   ```gml
   // Example of switching rooms using GML code
   if (place_meeting(x, y, obj_EndOfLevel))
   {
       room_goto(room_Level2);
   }
   ```

4. **Setting Persistent Objects:**
   - Sometimes you might want certain objects to persist across multiple rooms, such as a health bar or score counter. You can set an object to be persistent by checking the “Persistent” box in its properties.
   ```gml
   // Example of setting an object to be persistent in GML code
   instance_create_layer(x, y, "Instances", obj_Score);
   obj_Score.persistent = true;
   ```

Rooms are a fundamental aspect of GameMaker Studio 2 that allow developers to create organized and modular game levels. They provide the structure needed to build complex and engaging games by managing different scenes and their elements efficiently.

#Rooms #GameMaker