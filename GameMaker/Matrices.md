### Matrices in GameMaker

In GameMaker Studio 2 (GMS2), matrices are used primarily for transformations such as scaling, rotating, and translating objects or drawing surfaces. A matrix can be thought of as a way to store these transformations mathematically so that they can be applied efficiently.

#### Matrix Basics
A transformation matrix in 2D is typically a 3x3 grid of numbers, although it's often represented using a 1-dimensional array due to memory and performance considerations. The general form looks like this:

```
[ a, b, c ]
[ d, e, f ]
[ 0, 0, 1 ]  // This row is always [0, 0, 1] for affine transformations
```

The top-left 2x2 submatrix handles scaling and rotation:
- `a` and `e` control scaling along the x-axis and y-axis respectively.
- `b` and `d` are used for rotation.

The rightmost column (`c`, `f`) is used to translate (move) objects in 2D space.

#### Matrix Functions
GameMaker provides several functions to work with matrices:
- `matrix_build()` to create a transformation matrix from given scale, rotation, and translation.
- `matrix_get()` and `matrix_set()` to get and set values within the matrix.
- `matrix_multiply()` to combine two transformations into one.
- `matrix_apply()` applies a matrix to a position or vector.

#### Example: Using Matrices for Transformations
Here's an example of how you might use matrices in GML to scale, rotate, and translate a sprite:

```gml
// Create a new transformation matrix
var mat = matrix_build(xscale, yscale, rotation, x, y);

// Draw the sprite using the transformation matrix
draw_sprite_ext(sprite_index, image_index, 0, 0, xscale, yscale, rotation, c_white, 1, mat);
```

In this example:
- `xscale` and `yscale` are used to scale the sprite.
- `rotation` is used to rotate the sprite around its origin.
- `x` and `y` specify the position of the sprite's origin.

The `matrix_build()` function creates a matrix from these values. The `draw_sprite_ext()` function then uses this matrix for rendering, applying all transformations in one go.

#Matrices #GameMaker