### Understanding Effects in GameMaker

In GameMaker Studio 2 (GMS2), effects are visual enhancements that can be applied to draw calls, surfaces, or even entire rooms. These effects are typically implemented using shaders, which are small programs that run on the GPU to perform real-time graphical transformations and calculations. Effects can range from simple color adjustments like grayscale or sepia tone to complex distortions and lighting effects.

#### How to Use Effects

1. **Creating a Shader:**
   - Open GameMaker Studio 2.
   - Navigate to the Resource Tree and right-click on Shaders, then select "Create New Shader."
   - This will create two files: one for the vertex shader (`.vert`) and another for the fragment/pixel shader (`.frag`).
   
2. **Writing Shader Code:**
   - The vertex shader processes each vertex of a polygon before it is rasterized.
   - The fragment/pixel shader calculates the color for each pixel on the screen.

3. **Applying Shaders in GML:**
   - Use `shader_set()` to apply a shader before drawing.
   - Use `shader_reset()` to remove the current shader after drawing.
   
#### Example

Let's create a simple grayscale effect using shaders and apply it to a sprite in GameMaker Studio 2.

**Vertex Shader (default.vsh):**
```glsl
attribute vec3 in_Position;
attribute vec4 in_Colour;
attribute vec2 in_TextureCoord;

varying vec2 v_vTexcoord;
varying vec4 v_vColour;

void main()
{
    vec4 object_space_pos = vec4(in_Position.x, in_Position.y, in_Position.z, 1.0);
    gl_Position = gm_Matrices[MATRIX_WORLD_VIEW_PROJECTION] * object_space_pos;
    
    v_vTexcoord = in_TextureCoord;
    v_vColour = in_Colour;
}
```

**Fragment Shader (grayscale.fsh):**
```glsl
varying vec2 v_vTexcoord;
varying vec4 v_vColour;

uniform sampler2D gm_BaseTexture;

void main()
{
    vec4 col = texture2D(gm_BaseTexture, v_vTexcoord);
    float gray = dot(col.rgb, vec3(0.299, 0.587, 0.114));
    gl_FragColor = vec4(gray, gray, gray, col.a) * v_vColour;
}
```

**GML Code to Apply Shader:**
```gml
// Load shader
shader_grayscale = shader_get("grayscale_shader");

// Create a surface if needed
surface = surface_create(room_width, room_height);

draw_begin_surface(surface);
    draw_sprite(sprite_index, image_index, x, y); // Draw sprite on the surface
draw_end_surface();

// Apply the grayscale effect and draw the surface
shader_set(shader_grayscale);
draw_surface(surface, 0, 0);
shader_reset();
surface_free(surface);
```

In this example:
- We define a simple vertex shader that processes each vertex.
- The fragment shader converts colors to grayscale using the luminosity method (dot product with `[0.299, 0.587, 0.114]`).
- In GML, we apply the grayscale shader to a sprite drawn on a surface.

This allows for flexible and powerful visual effects in your games. #Effects #GameMaker