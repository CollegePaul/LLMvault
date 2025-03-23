### Understanding Surfaces in GameMaker

In GameMaker Studio 2 (GMS2), **surfaces** are used to render graphics off-screen. This means that you can draw onto a surface without immediately displaying it on the screen, which is useful for various purposes such as creating special effects, optimizing rendering performance, and more.

#### When to Use Surfaces
- **Off-Screen Rendering**: Draw complex scenes or effects without impacting the main game loop.
- **Effects**: Create visual effects like blurring, color shifting, etc., by manipulating surfaces.
- **Performance Optimization**: By drawing only once onto a surface and then repeatedly displaying that surface, you can reduce rendering overhead.

#### Basic Usage of Surfaces in GML

1. **Creating a Surface**
   ```gml
   // Create a new surface with the width and height specified
   var surf = surface_create(room_width, room_height);
   ```
   
2. **Drawing onto a Surface**
   ```gml
   // Begin drawing on the surface
   surface_set_target(surf);

   // Draw anything you want here, just like you would normally draw to the screen
   draw_rectangle(10, 10, 50, 50, false);
   draw_text(20, 30, "Hello Surface!");

   // End drawing on the surface and return to drawing directly to the screen
   surface_reset_target();
   ```
   
3. **Displaying a Surface**
   ```gml
   // Draw the contents of the surface onto the screen at position (100, 100)
   draw_surface(surf, 100, 100);
   ```
   
4. **Destroying a Surface**
   ```gml
   // Clean up and free the memory used by the surface when you're done with it
   surface_free(surf);
   ```

#### Example Scenario: Creating a Blurred Background

Here's how you might use surfaces to create a blurred background:

```gml
// Create Event of Object Controller
var bg_surface = surface_create(room_width, room_height);

// Draw the background onto the surface
surface_set_target(bg_surface);
draw_background(bck_BackgroundImage); // Replace with your background resource name
surface_reset_target();

// Apply a blur effect to the surface (this is just an example; actual blurring might require shaders)
var blurred_surface = surface_create(room_width, room_height);
surface_set_target(blurred_surface);

// Draw the original surface onto the new one using a blur shader or similar technique
draw_surface_ext(bg_surface, 0, 0, 1, 1, 0, c_white, 1); // Normally apply blur here

surface_reset_target();

// Clean up
surface_free(bg_surface);
```

In the `Draw Event` of an object:

```gml
// Draw the blurred background surface to the screen
draw_surface(blurred_surface, 0, 0);

// Don't forget to free the final surface when done (could be in End Room event)
surface_free(blurred_surface);
```

#Surfaces #GameMaker