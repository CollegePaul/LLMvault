### Button Commands in Tkinter

In Tkinter, a popular GUI toolkit for Python, buttons can be configured to execute specific functions or commands when they are clicked. This functionality is achieved by using the `command` parameter of the `Button` widget. The `command` parameter takes a function name (without parentheses) as its value, and this function will be called whenever the button is pressed.

Here's how you can create a simple application with a button that prints a message to the console when clicked:

```python
import tkinter as tk

def on_button_click():
    print("Button was clicked!")

# Create the main window
root = tk.Tk()
root.title("Tkinter Button Example")

# Create a button and set its command
button = tk.Button(root, text="Click Me!", command=on_button_click)
button.pack(pady=20)

# Start the Tkinter event loop
root.mainloop()
```

In this example:
- We import the `tkinter` module.
- Define a function `on_button_click()` that prints "Button was clicked!" to the console.
- Create the main application window using `tk.Tk()`.
- Instantiate a `Button` widget, setting its text to "Click Me!" and assigning the `on_button_click` function as the command.
- Use `button.pack(pady=20)` to add the button to the window with some vertical padding.
- Call `root.mainloop()` to start the Tkinter event loop, which keeps the window open and responsive.

This simple setup demonstrates how to use button commands in Tkinter to trigger actions in response to user interactions. #Button Commands #TKinter #Python