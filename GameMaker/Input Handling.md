### Input Handling in GameMaker

In GameMaker Studio 2 (GMS2), input handling is crucial for creating interactive games where players can control characters, navigate menus, or perform actions. The most common types of inputs handled are keyboard, mouse, and gamepad inputs.

#### Keyboard Input

Keyboard input is managed using functions that check the state of individual keys. For example, to move a player character left when the 'A' key is pressed, you can use `keyboard_check()`:

```gml
if (keyboard_check(vk_a)) {
    x -= 5; // Move the object 5 pixels to the left
}
```

In this code snippet, `vk_a` represents the ASCII value for the 'A' key. The function `keyboard_check()` returns true if the specified key is currently pressed.

#### Mouse Input

Mouse input involves checking mouse button states and position using functions like `mouse_check_button()` and `mouse_x`, `mouse_y`. To shoot a projectile when the left mouse button is clicked, you can use:

```gml
if (mouse_check_button_released(mb_left)) {
    instance_create(mouse_x, mouse_y, obj_projectile);
}
```

Here, `mb_left` checks for the left mouse button. The function `mouse_check_button_released()` returns true if the button was released during the previous step.

#### Gamepad Input

Gamepad input is slightly more complex but equally important for games that support controller inputs. You need to check each gamepad's state and individual buttons or axes using functions like `gamepad_button_check()` and `gamepad_axis_value()`. To move a character with the left stick of a connected gamepad, you might use:

```gml
var pad_id = 0; // Assuming the first controller is used

var horizontal_movement = gamepad_axis_value(pad_id, gp_axislh);
var vertical_movement = gamepad_axis_value(pad_id, gp_axislv);

x += horizontal_movement * 5;
y += vertical_movement * 5;
```

In this example, `gp_axislh` and `gp_axislv` refer to the left stick's horizontal and vertical axes respectively. The function `gamepad_axis_value()` returns a value between -1 and 1 for each axis.

### #Input Handling
### #GamaMaker