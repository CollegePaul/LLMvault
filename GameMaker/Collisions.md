### Collisions in GameMaker

In GameMaker Studio 2 (GMS2), collisions refer to interactions between objects within your game world. These interactions can involve physics-based collision detection, where physical bodies interact according to real-world physics principles, or they can be based on simpler bounding box or precise mask detection.

#### Types of Collisions
1. **Bounding Box Collision**: This is the simplest form of collision detection in GameMaker. Each object has a rectangular bounding box that determines its hit area. If two objects' bounding boxes overlap, a collision is detected.
   
2. **Mask Collision**: Mask collision uses a more precise method where each object can have a custom shape defined by a mask image. Collisions are detected based on the actual pixels of these masks.

3. **Physics-Based Collision**: This involves using GameMaker's physics engine to detect collisions between objects that have been assigned physical properties such as mass, gravity, and restitution (bounciness).

#### Example: Bounding Box Collision

Here is a simple example of how you can check for bounding box collision in GML:

```gml
// Assuming obj_player and obj_enemy are your object names
if (place_meeting(x, y, obj_enemy))
{
    show_debug_message("Collision detected with enemy!");
}
```

In this script, `place_meeting()` checks if the instance of `obj_player` at its current position `(x, y)` is colliding with any instances of `obj_enemy`.

#### Example: Mask Collision

To use mask collision, you need to ensure that your objects have a sprite assigned as their mask. Here’s how you can check for collisions using masks:

```gml
// Assuming obj_player and obj_enemy are your object names
if (instance_place(x, y, obj_enemy))
{
    show_debug_message("Mask collision detected with enemy!");
}
```

`instance_place()` checks for collisions based on the mask of `obj_player` at its current position `(x, y)` with any instances of `obj_enemy`.

#### Example: Physics-Based Collision

First, you need to enable physics for your objects in their object properties or via code:

```gml
// Enable physics for obj_player and obj_enemy
physics_enabled = true;
```

Then, you can use collision events such as `on_collision` to detect collisions. Here’s an example of how you might handle a collision event in GML:

```gml
/// Collision Event with obj_enemy
show_debug_message("Physics collision detected with enemy!");
// Example response: Apply damage or knockback
health -= 10;
```

This script is placed in the `obj_player` object’s collision event, and it will be executed whenever `obj_player` collides with an instance of `obj_enemy`.

#Collisions #GameMaker