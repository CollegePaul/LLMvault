### IntVar Class in Tkinter

The `IntVar` class in Tkinter is used to manage integer variables that are associated with widgets such as Checkbuttons, Radiobuttons, and Scale. It provides a way to track changes in the value of an integer variable in a user-friendly manner.

When you create an instance of `IntVar`, it initializes with a default value of 0 unless specified otherwise. You can use methods like `get()` to retrieve the current value of the variable and `set(value)` to update its value.

Here is an example demonstrating how to use `IntVar` with a Radiobutton widget:

```python
import tkinter as tk

# Create the main window
root = tk.Tk()
root.title("IntVar Example")

# Create an IntVar object
selected_option = tk.IntVar()

# Set the default value of the IntVar
selected_option.set(1)

# Define a function to display the selected option
def show_selection():
    print(f"Selected Option: {selected_option.get()}")

# Create Radiobutton widgets
radio_button_1 = tk.Radiobutton(root, text="Option 1", variable=selected_option, value=1)
radio_button_2 = tk.Radiobutton(root, text="Option 2", variable=selected_option, value=2)
radio_button_3 = tk.Radiobutton(root, text="Option 3", variable=selected_option, value=3)

# Create a Button to display the selected option
show_button = tk.Button(root, text="Show Selection", command=show_selection)

# Pack the widgets
radio_button_1.pack()
radio_button_2.pack()
radio_button_3.pack()
show_button.pack()

# Start the Tkinter event loop
root.mainloop()
```

In this example:
- An `IntVar` object named `selected_option` is created and initialized with a value of 1.
- Three Radiobutton widgets are created, each associated with the same `IntVar` object but having different values (1, 2, and 3).
- When a user selects a radiobutton, the `selected_option` variable updates to reflect the selected value.
- A button is provided that, when clicked, calls the `show_selection` function, which prints the current value of `selected_option`.

#IntVar Class #TKinter #Python