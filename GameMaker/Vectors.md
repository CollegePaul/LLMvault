### Understanding Vectors in GameMaker

In GameMaker, vectors are essential tools used to represent quantities that have both magnitude (size) and direction. They are commonly used for movement, forces, velocity, and acceleration of game objects. A vector is typically defined using two or three components representing its direction along the x-axis, y-axis, and optionally the z-axis in 3D space.

#### Basic Operations with Vectors

1. **Creating a Vector:**
   You can create a vector by defining its components directly.
   ```gml
   // Create a vector with x component of 5 and y component of 10
   var vector = vector_create(5, 10);
   ```

2. **Adding Vectors:**
   Vectors can be added to represent combined movements or forces.
   ```gml
   // Define two vectors
   var vector_a = vector_create(3, 4);
   var vector_b = vector_create(6, 8);

   // Add the vectors
   var resultant_vector = vector_add(vector_a, vector_b);
   ```

3. **Scaling a Vector:**
   Vectors can be scaled by multiplying them with a scalar to adjust their magnitude.
   ```gml
   // Define a vector
   var vector_c = vector_create(2, 5);

   // Scale the vector by a factor of 3
   var scaled_vector = vector_scale(vector_c, 3);
   ```

4. **Dot Product:**
   The dot product is used to find the angle between two vectors or to project one vector onto another.
   ```gml
   // Define two vectors
   var vector_d = vector_create(1, 0);
   var vector_e = vector_create(0, 1);

   // Calculate the dot product
   var dot_product = vector_dot_product(vector_d, vector_e);
   ```

5. **Magnitude of a Vector:**
   The magnitude (length) of a vector can be calculated using `vector_length()`.
   ```gml
   // Define a vector
   var vector_f = vector_create(3, 4);

   // Calculate the magnitude
   var length = vector_length(vector_f);
   ```

Vectors are fundamental in physics-based games for handling motion and interactions. By leveraging vectors, developers can create realistic movements and reactions within their game environments.

#Vectors #GamaMaker