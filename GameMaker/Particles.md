### Particles in GameMaker

Particles in GameMaker are used to create dynamic visual effects such as smoke, fire, explosions, and rain. They simulate small objects that move in an environment according to certain rules defined by the user. Particles can significantly enhance the visual appeal of a game without requiring complex animations or sprite sheets.

To use particles, you first need to define a particle system and then create particle types within that system. Each particle type has properties like size, color, speed, direction, and lifetime which determine how the particles behave on screen.

#### Example in GML:

1. **Create Particle System:**
   ```gml
   // Create a new particle system
   global.psys = part_system_create();
   ```

2. **Create Particle Type:**
   ```gml
   // Define a new particle type for smoke
   global.ptype_smoke = part_type_create();

   // Set properties of the particle type
   part_type_shape(global.ptype_smoke, pt_shape_circle); // Shape is circular
   part_type_size(global.ptype_smoke, 0.1, 2, -0.01);    // Size changes over time
   part_type_scale(global.ptype_smoke, 1, 2);            // Scale from 1 to 2
   part_type_color3(global.ptype_smoke, c_white, c_gray, c_black); // Color transition
   part_type_alpha3(global.ptype_smoke, 0.8, 0.5, 0);     // Alpha transition
   part_type_speed(global.ptype_smoke, 1, 2, 0);          // Speed range and acceleration
   part_type_direction(global.ptype_smoke, 0, 360, 0);    // Direction range
   part_type_life(global.ptype_smoke, 15, 30);            // Lifetime of the particles
   ```

3. **Emit Particles:**
   ```gml
   // Emit smoke particles from object position
   part_particles_create(global.psys, x, y, global.ptype_smoke, 5);
   ```

4. **Draw Particle System:**
   Ensure to draw the particle system in the Draw event of an object or room:
   ```gml
   // Draw the particle system
   part_system_draw(global.psys);
   ```

5. **Clean Up:**
   When you no longer need the particle system, clean it up to free resources.
   ```gml
   // Destroy the particle type and system
   part_type_destroy(global.ptype_smoke);
   part_system_destroy(global.psys);
   ```

Particles are a powerful tool for adding atmospheric effects to games, making them more engaging and visually interesting. #Particles #GamaMaker