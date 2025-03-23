### Physics in GameMaker

GameMaker includes a physics engine that allows developers to simulate real-world physics behaviors within their games. This can involve gravity, collisions, joints, and other physical interactions between game objects. The physics system uses concepts like mass, friction, restitution (bounciness), and density to make the game world feel more realistic.

To use the physics engine in GameMaker, you must first enable it either globally or for individual rooms. Once enabled, you can assign physics properties to objects, which then interact with each other according to the laws of physics defined by the engine.

#### Example: Creating a Simple Ball Falling

Let's create a simple example where we have a ball object that falls due to gravity:

1. **Enable Physics in the Room**:
   - Open your room in GameMaker Studio 2.
   - In the Room Properties, go to the Physics tab and check "Use physics world."

2. **Create a Ball Object**:
   - Create an object named `obj_ball`.
   - Add a sprite to this object that represents a ball.

3. **Assign Physics Properties**:
   - Go to the object's properties in GameMaker Studio 2.
   - Navigate to the Physics tab and check "Use physics".
   - Set the shape type to Circle, adjust the radius according to your sprite, and set other properties like density, friction, and restitution.

4. **Add Code to Create Ball Instances**:
   - In an event (like `Create` or `Room Start`) of another object or the room itself, use the following code to create a ball instance:

```gml
// Create an instance of obj_ball at position (320, 50)
instance_create_layer(320, 50, "Instances", obj_ball);
```

5. **Observe Gravity**:
   - Run your game and you should see the ball fall due to gravity.

This simple setup demonstrates how physics can be used in GameMaker to simulate falling objects. You can expand on this by adding more objects with different shapes and properties, creating platforms for the ball to bounce off of, or even adding forces like wind using `physics_apply_force` function.

#Physics #GameMaker