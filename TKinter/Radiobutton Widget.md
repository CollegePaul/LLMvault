### Radiobutton Widget in Tkinter

The Radiobutton widget in Tkinter provides a way to select one option from a set of options. Each radiobutton is associated with a variable, which holds the value of the selected option. When one radiobutton is selected, all others in the same group are deselected automatically.

Here's a simple example demonstrating how to use Radiobuttons:

```python
import tkinter as tk

def show_choice():
    print(f"Selected option: {var.get()}")

# Create the main window
root = tk.Tk()
root.title("Radiobutton Example")

# Variable to hold the selected value
var = tk.StringVar(value="Option 1")  # Default value

# Creating Radiobuttons
option1 = tk.Radiobutton(root, text="Option 1", variable=var, value="Option 1", command=show_choice)
option2 = tk.Radiobutton(root, text="Option 2", variable=var, value="Option 2", command=show_choice)
option3 = tk.Radiobutton(root, text="Option 3", variable=var, value="Option 3", command=show_choice)

# Packing Radiobuttons
option1.pack()
option2.pack()
option3.pack()

root.mainloop()
```

In this example:
- We import the `tkinter` module.
- A function `show_choice()` is defined to print the selected option whenever a radiobutton is clicked.
- A main window (`root`) is created with a title.
- A `StringVar` variable named `var` holds the value of the currently selected radiobutton. It's initialized with "Option 1" as the default value.
- Three Radiobuttons are created, each associated with the same variable `var`, but having different values ("Option 1", "Option 2", and "Option 3").
- The `command` parameter is used to specify the function to call when a radiobutton is clicked.
- Finally, the main event loop is started with `root.mainloop()`.

#Radiobutton Widget #TKinter #Python