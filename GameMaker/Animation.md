### Understanding Animation in GameMaker

In GameMaker, animation is a fundamental aspect that brings life to your game's characters, objects, and environments. It involves creating sequences of images or sprites that change over time, simulating movement and other dynamic behaviors.

#### How to Create an Animation

1. **Create Sprites**: Start by importing image assets into GameMaker Studio 2 as sprites. Each sprite can have multiple sub-images which represent different frames of the animation.
   
2. **Setup Animation Frames**: Use the Sprite Editor to arrange these sub-images in a specific order that represents the movement or action you want to animate.

3. **Animate Sprites in Objects**: Attach the sprite to an object and use scripts or event actions to control when and how the sprite animates.

#### Using GML for Animation

GameMaker Language (GML) allows for precise control over animations. Here are some common functions used:

- `sprite_index`: Sets or retrieves the current sprite being displayed.
- `image_speed`: Adjusts the speed of the animation by setting the number of frames to advance per game frame.
- `image_xscale` and `image_yscale`: Scales the sprite horizontally and vertically, useful for resizing animations dynamically.
- `image_angle`: Rotates the sprite around its origin point.

#### Example: Simple Walking Animation

Let's create a basic walking animation for an object called `obj_player`.

1. **Sprite Setup**:
   - Create a new sprite named `spr_player_walk` with several sub-images showing different phases of a walk cycle.
   
2. **Object Creation Code**:
   ```gml
   // Set the initial sprite and its speed
   sprite_index = spr_player_walk;
   image_speed = 0.1;  // Slower animation to make it look more natural
   ```

3. **Step Event for Movement**:
   ```gml
   // Check if player is moving horizontally
   if (keyboard_check(vk_right)) {
       x += 4;         // Move right by 4 pixels per frame
       image_xscale = 1; // Ensure the sprite faces right
   } else if (keyboard_check(vk_left)) {
       x -= 4;         // Move left by 4 pixels per frame
       image_xscale = -1; // Flip the sprite horizontally to face left
   }
   
   // Stop the animation if no keys are pressed
   if (!keyboard_check(vk_right) && !keyboard_check(vk_left)) {
       image_speed = 0;
   } else {
       image_speed = 0.1; // Resume walking speed
   }
   ```

This code snippet ensures that when the player presses the left or right arrow keys, the `obj_player` object moves and animates accordingly. When no keys are pressed, the animation stops.

#Animation #GameMaker