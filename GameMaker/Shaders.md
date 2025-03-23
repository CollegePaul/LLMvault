### Shaders in GameMaker

Shaders are small programs that run on the GPU to process graphics. In GameMaker Studio 2, shaders can be used to create advanced visual effects like blurring, lighting, color grading, and more. They consist of two main types of code: Vertex Shader (which processes vertices) and Fragment Shader (which processes pixels).

**Creating a Simple Shader in GameMaker**

To use shaders, you first need to write the shader code in GLSL (OpenGL Shading Language). Here’s an example of how to create a simple grayscale effect using a fragment shader.

1. **Create a New Shader Object:**
   - In GameMaker Studio 2, go to `Resources` > `Shaders`.
   - Right-click and select `Create Shader`. Name it something like `sh_grayscale`.

2. **Write the Fragment Shader Code:**
   - Open the newly created shader resource.
   - Write the following code in the `Fragment Shader` section:

```glsl
varying vec2 v_vTexcoord;
uniform sampler2D gm_BaseTexture;

void main()
{
    vec4 color = texture2D(gm_BaseTexture, v_vTexcoord);
    float grayscale = dot(color.rgb, vec3(0.299, 0.587, 0.114));
    gl_FragColor = vec4(grayscale, grayscale, grayscale, color.a);
}
```

This code takes the color of each pixel, converts it to grayscale using a weighted sum of its RGB components, and then outputs the new grayscale color.

3. **Using the Shader in GML:**
   - To apply this shader to an object or a specific draw call, you need to use some GML functions.
   - Here’s an example of how to apply the shader to a sprite being drawn:

```gml
// In your Draw event or Step event where rendering occurs

// Start drawing with the shader applied
shader_set(sh_grayscale);

// Your normal drawing code here
draw_sprite(spr_player, 0, x, y);

// Stop using the shader
shader_reset();
```

In this example, `sh_grayscale` is the name of your shader resource. `sprite_draw` will render with the grayscale effect applied.

Shaders are powerful tools in GameMaker Studio 2 that can greatly enhance the visual appeal and performance of games by offloading processing tasks to the GPU. #Shaders #GameMaker