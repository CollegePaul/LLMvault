### Cameras in GameMaker

In GameMaker Studio 2, cameras are used to control what portion of the game world is visible on the screen. This can be particularly useful for creating effects like following a player character or showing different perspectives in complex scenes.

#### Basic Usage

To use cameras, you typically start by defining them and then setting their properties such as position and size. Here's an example of how to create a camera that follows a player object:

```gml
// Create Event - Object Player Controller
camera_create(camera_main);
camera_set_viewport(camera_main, 0, 0, room_width, room_height);
camera_set_begin_script(camera_main, cameramain_begin);
```

In this snippet, `camera_main` is created and set to cover the entire room. The `camera_set_begin_script` function sets a script that runs before drawing the view associated with the camera.

```gml
// cameramain_begin - Script
var player = instance_find_first(oPlayer);  // Assuming oPlayer is your player object
if (player != noone)
{
    camera_set_view_pos(camera_main, player.x - room_width/2, player.y - room_height/2);
}
```

This script finds the player object and sets the camera's view position so that it always centers on the player. This creates a "follow" effect where the player is always in the middle of the screen.

#### Multiple Cameras

You can also use multiple cameras to show different views or layers simultaneously. Here’s how you might set up two cameras, one for the main game area and another for an overhead view:

```gml
// Create Event - Controller Object
camera_create(camera_main);
camera_set_viewport(camera_main, 0, 0, room_width, room_height);
camera_set_begin_script(camera_main, cameramain_begin);

camera_create(camera_overhead);
camera_set_viewport(camera_overhead, room_width/2, 0, room_width/2, room_height/2);
camera_set_begin_script(camera_overhead, cameraoverhead_begin);
```

In the `cameraoverhead_begin` script:

```gml
// cameraoverhead_begin - Script
var player = instance_find_first(oPlayer); // Assuming oPlayer is your player object
if (player != noone)
{
    camera_set_view_pos(camera_overhead, player.x - room_width/4, player.y - room_height/2);
}
camera_set_angle(camera_overhead, 90);
```

This script positions the overhead camera to follow the player but with a rotated view.

### Summary

Cameras in GameMaker are a powerful tool for controlling what players see and can greatly enhance the visual experience of your game. By using scripts like `begin` and `end`, you can dynamically change camera properties based on gameplay events, leading to more engaging and immersive levels.

#GameMaker #Cameras