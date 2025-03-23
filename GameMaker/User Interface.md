### User Interface in GameMaker

In GameMaker Studio 2 (GMS2), the User Interface (UI) refers to all elements that allow players to interact with your game, such as buttons, sliders, text input fields, checkboxes, dropdown menus, and more. These UI elements are essential for creating menus, settings screens, HUDs (heads-up displays), and other interactive components.

#### Creating a Simple Button

To create a simple button in GameMaker, you can use the `draw_sprite` function to draw an image that acts as the button and then handle mouse input to detect when the button is clicked. Here’s a basic example using GML:

1. **Create a Sprite for the Button:**
   - Create two sprites: one for the normal state (`spr_button_normal`) and another for the pressed state (`spr_button_pressed`).

2. **Create an Object for the Button:**
   - In GameMaker, create a new object (e.g., `obj_Button`).
   - Add code to draw the button sprite in the `Draw GUI` event.
   - Handle mouse input in the `Step` or `Begin Step` event.

```gml
// Inside obj_Button Create Event
normal_sprite = spr_button_normal;
pressed_sprite = spr_button_pressed;
is_pressed = false;

// Inside obj_Button Draw GUI Event
if (is_pressed) {
    draw_sprite(pressed_sprite, 0, x, y);
} else {
    draw_sprite(normal_sprite, 0, x, y);
}

// Inside obj_Button Step Event
var mouse_x = mouse_x - view_xview[view_current];
var mouse_y = mouse_y - view_yview[view_current];

if (mouse_check_button(mb_left)) {
    if (point_in_rectangle(mouse_x, mouse_y, x, y, x + sprite_get_width(normal_sprite), y + sprite_get_height(normal_sprite))) {
        is_pressed = true;
        // Add action to perform when button is pressed
        show_debug_message("Button Clicked!");
    }
} else {
    is_pressed = false;
}
```

#### Explanation

- **Sprites:** `spr_button_normal` and `spr_button_pressed` are used to visually represent the button in its normal and pressed states.
- **Mouse Detection:** The script checks if the mouse cursor is within the boundaries of the button sprite. If the left mouse button is clicked while the cursor is over the button, the button’s state changes to pressed.
- **Action on Click:** In this example, a debug message is shown when the button is clicked.

This basic setup can be expanded with additional functionality, such as animations, sound effects, or more complex interactions. GameMaker provides various functions and events for creating interactive UI elements, making it flexible for developers to implement custom interfaces.

#User Interface #GamaMaker