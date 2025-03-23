### Sprites in GameMaker

Sprites are graphical assets that can be used to represent characters, objects, or any other visual elements within a game environment in GameMaker Studio. Essentially, a sprite is an image file that you import into your project and then use to create instances (known as objects) on the screen. Sprites can have multiple sub-images, which allows for animations.

#### Example Usage in GML

Let's consider a simple example where we create a player character that uses a single sprite with multiple frames to animate walking:

1. **Importing a Sprite:**
   - You would first import your sprite into the resource tree by right-clicking on `Sprites` and selecting `Create Sprite`. Then, you can add images to this sprite.

2. **Using the Sprite in an Object:**
   - Create an object called `obj_Player`.
   - In the `Create Event` of `obj_Player`, initialize variables for movement.
     ```gml
     // Set initial speed and direction
     hspeed = 0;
     vspeed = 0;
     walk_speed = 4;

     // Set sprite index to the first frame
     image_index = 0;
     ```
   - In the `Step Event` of `obj_Player`, add code for movement and animation.
     ```gml
     // Handle input for walking
     if (keyboard_check(vk_right)) {
         hspeed = walk_speed;
         sprite_index = spr_player_walk; // Assume 'spr_player_walk' is your animated sprite
         image_xscale = 1; // Face right
     } else if (keyboard_check(vk_left)) {
         hspeed = -walk_speed;
         sprite_index = spr_player_walk;
         image_xscale = -1; // Face left
     } else {
         hspeed = 0;
         image_index = 0; // Stand still on the first frame of the sprite
     }

     // Move the object according to speed
     x += hspeed;
     y += vspeed;

     // Update animation frame automatically based on walk_speed
     image_speed = 0.2; // Controls how fast the frames change
     ```

In this example, `spr_player_walk` is a sprite that has multiple sub-images representing different walking poses. The `image_index` variable controls which frame of the sprite is displayed, and the `image_speed` variable determines how quickly the animation progresses through its frames.

#Sprites #GameMaker