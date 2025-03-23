### Views in GameMaker

In GameMaker, views are rectangular areas that define what part of the room (or game world) is visible to the player. This feature is particularly useful for creating larger worlds than the screen can display all at once. Views allow developers to control exactly which parts of a room are drawn on the screen, enabling smooth camera movements and transitions between different areas.

You can have up to eight views active at any time in GameMaker Studio 2. Each view can be set to follow an object, allowing for dynamic camera movement that tracks the player or another character as they move around the room. Views also give you control over how and where the portion of the room is displayed on the screen.

Here’s a basic example using GML code to create and manipulate views:

```gml
// Create event of an object (e.g., obj_camera_controller)
view_enabled[0] = true; // Enable view 0
view_visible[0] = true; // Make sure the view is visible

// Set the port on the screen that the view will draw to
view_xport[0] = 0;
view_yport[0] = 0;
view_wport[0] = display_get_width();
view_hport[0] = display_get_height();

// Set the area of the room that the view will look at
view_xview[0] = room_width / 2 - view_wport[0] / 2;
view_yview[0] = room_height / 2 - view_hport[0] / 2;
view_wview[0] = view_wport[0];
view_hview[0] = view_hport[0];

// Set the view to follow an object
var objToFollow = instance_find_nearest(object_player, 1);
if (instance_exists(objToFollow))
{
    view_object_index[0] = objToFollow;
}
```

In this example:
- A single view (`view[0]`) is enabled and made visible.
- The port of the view is set to match the size of the game window.
- The area of the room that the view displays is centered around the middle of the room, initially.
- Finally, the view is set to follow an instance of `object_player`.

This setup allows for a dynamic camera system where the view follows the player object as it moves within the room. #Views #GamaMaker