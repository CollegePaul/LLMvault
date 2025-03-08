### Button Widget in Tkinter

The Button widget in Tkinter is used to create clickable buttons that can trigger actions when clicked by the user. This widget is essential for creating interactive GUI applications. It allows you to define various properties such as text, command, background color, foreground color, and more.

Here’s a simple example of how to use the Button widget in Python with Tkinter:

```python
import tkinter as tk

def on_button_click():
    print("Button was clicked!")

# Create the main window
root = tk.Tk()
root.title("Tkinter Button Example")

# Create a button widget
button = tk.Button(root, text="Click Me!", command=on_button_click)

# Place the button in the window
button.pack(pady=20)

# Start the Tkinter event loop
root.mainloop()
```

In this example:
- We import the `tkinter` module.
- Define a function `on_button_click` that prints a message when called.
- Create the main application window using `tk.Tk()`.
- Instantiate a Button widget with the text "Click Me!" and set its command to the `on_button_click` function.
- Use the `pack()` method to add the button to the window with some vertical padding.
- Finally, start the Tkinter event loop with `root.mainloop()` to keep the application running.

This simple setup demonstrates how a Button widget can be used to handle user interactions in a Tkinter application. #Button Widget #TKinter #Python