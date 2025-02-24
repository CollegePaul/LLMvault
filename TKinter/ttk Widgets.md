### ttk Widgets in Tkinter

The `ttk` module in Tkinter provides access to the newer themed widgets, which offer a more modern look and feel compared to the traditional Tkinter widgets. These widgets are part of the Tile widget set, which was originally developed for Tcl/Tk but is also available in Python through Tkinter.

Some common ttk widgets include:
- **Button**: A button that can contain text and/or an image.
- **Label**: Displays a short string or an image.
- **Entry**: Allows the user to enter or edit a single line of text.
- **Frame**: Used as a container widget to hold other widgets.
- **Combobox**: Combines a label or entry field with a drop-down list.
- **Checkbutton**: A button that can be toggled between selected and not selected states.
- **Radiobutton**: One of several buttons in a group, only one of which can be selected at any time.
- **Progressbar**: Displays the progress of an ongoing task.
- **Notebook**: A collection of tabs.

Here is a simple example demonstrating the use of some ttk widgets:

```python
import tkinter as tk
from tkinter import ttk

# Create the main window
root = tk.Tk()
root.title("ttk Widgets Example")

# Create a frame to hold widgets
frame = ttk.Frame(root, padding="10")
frame.grid(row=0, column=0, sticky=(tk.W, tk.E, tk.N, tk.S))

# Add a label
label = ttk.Label(frame, text="Enter your name:")
label.grid(row=0, column=0, padx=5, pady=5)

# Add an entry widget
entry = ttk.Entry(frame)
entry.grid(row=0, column=1, padx=5, pady=5)

# Add a button that prints the entry value
def on_button_click():
    print(f"Hello, {entry.get()}!")

button = ttk.Button(frame, text="Greet", command=on_button_click)
button.grid(row=1, column=0, columnspan=2, pady=10)

# Configure grid weights to make the frame expandable
root.columnconfigure(0, weight=1)
root.rowconfigure(0, weight=1)
frame.columnconfigure(1, weight=1)

# Start the main event loop
root.mainloop()
```

In this example:
- A `ttk.Frame` is used as a container.
- A `ttk.Label` prompts the user for their name.
- A `ttk.Entry` widget allows the user to input text.
- A `ttk.Button` triggers an action when clicked, which prints a greeting message using the entered text.

#ttk Widgets #TKinter #Python