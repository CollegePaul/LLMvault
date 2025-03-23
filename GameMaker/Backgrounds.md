### Backgrounds in GameMaker

In GameMaker Studio, backgrounds are used to create static visual elements that appear behind or within your game's rooms. These can range from simple color fills to complex images like tilesets or intricate scenes. Backgrounds are an essential part of the room editor and play a significant role in setting up the environment where your game takes place.

#### How to Use Backgrounds

1. **Creating a New Background**: You can create new backgrounds by right-clicking on the 'Backgrounds' folder in the Resource Tree and selecting 'Create Background'. This opens an editor where you can draw directly or import images as backgrounds.

2. **Applying a Background to a Room**: To add a background to a room, open the room editor and go to the "Background" tab. Here, you can choose which background(s) you want to use and position them within the room grid.

3. **Using GML with Backgrounds**: While backgrounds are primarily managed through the room editor, GameMaker's scripting language (GML) allows for more dynamic control over how they are displayed. You can change backgrounds, adjust their positions, or even scale them using code.

#### Example Using GML

Here is a simple example of how you might use GML to dynamically switch backgrounds in a game:

```gml
// Assume 'bg_day' and 'bg_night' are the names of your background resources
if (hour( current_time ) >= 18 || hour( current_time ) < 6)
{
    room_set_background_image(room, 0, bg_night);
}
else
{
    room_set_background_image(room, 0, bg_day);
}
```

In this example:
- We check the current time using `current_time` and extract the hour with `hour()`.
- If it's between 6 PM (18) and 6 AM, we set the background to `bg_night`.
- Otherwise, we set it to `bg_day`.

This script could be placed in an event like `Step` or `Create` depending on when you want the background change to occur.

#Backgrounds #GameMaker