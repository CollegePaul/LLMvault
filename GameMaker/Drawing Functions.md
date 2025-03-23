### Drawing Functions in GameMaker

In GameMaker Studio 2 (GMS2), drawing functions are essential tools used to render graphics, text, shapes, and other visual elements onto the screen during game execution. These functions allow developers to have precise control over how and where things appear on the display surface. Below are some common drawing functions along with examples of their usage in GML (GameMaker Language).

#### Common Drawing Functions:

1. **`draw_sprite()`** - Draws a sprite at a specified position.
    ```gml
    // Draw the first frame of 'spr_player' at position (100, 200)
    draw_sprite(spr_player, 0, 100, 200);
    ```

2. **`draw_rectangle()`** - Draws a rectangle.
    ```gml
    // Draw an unfilled red rectangle from (50, 50) to (200, 100)
    draw_set_color(c_red);
    draw_rectangle(50, 50, 200, 100, false);
    ```

3. **`draw_text()`** - Draws text at a specified position.
    ```gml
    // Draw "Hello, World!" in white at (100, 300)
    draw_set_color(c_white);
    draw_text(100, 300, "Hello, World!");
    ```

4. **`draw_circle()`** - Draws a circle.
    ```gml
    // Draw an unfilled blue circle at (250, 250) with radius 50
    draw_set_color(c_blue);
    draw_circle(250, 250, 50, false);
    ```

5. **`draw_line()`** - Draws a line between two points.
    ```gml
    // Draw a green line from (100, 350) to (250, 450)
    draw_set_color(c_green);
    draw_line(100, 350, 250, 450);
    ```

These functions can be used in various scripts and events within your game objects, such as `Draw` event or custom scripts called from other events.

#Drawing Functions #GameMaker