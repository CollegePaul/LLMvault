### Listbox Widget in Tkinter

The Listbox widget in Tkinter is used to display a list of items from which a user can select one or more options. It provides a simple way to create lists that can be navigated using the keyboard, mouse, or programmatically. The Listbox widget supports various operations such as adding, deleting, and selecting items.

To use a Listbox, you first need to import Tkinter and then create an instance of the `Listbox` class. Items can be added to the list using the `insert()` method, where you specify the index at which to insert the item and the item itself. You can also configure various options like height, width, and selection mode.

Here is a simple example demonstrating how to use the Listbox widget in Tkinter:

```python
import tkinter as tk

# Create the main window
root = tk.Tk()
root.title("Listbox Example")

# Create a Listbox widget
listbox = tk.Listbox(root)
listbox.pack(padx=10, pady=10)

# Add items to the listbox
items = ["Apple", "Banana", "Cherry", "Date", "Elderberry"]
for item in items:
    listbox.insert(tk.END, item)

# Function to display selected item(s)
def show_selection():
    # Get the index of the selected item
    selection_indices = listbox.curselection()
    # Get the text of the selected item(s)
    selected_items = [listbox.get(i) for i in selection_indices]
    print("Selected items:", selected_items)

# Create a button to display selected item(s)
button = tk.Button(root, text="Show Selection", command=show_selection)
button.pack(pady=10)

# Run the application
root.mainloop()
```

In this example:
- A Tkinter window is created.
- A Listbox widget is added to the window with a list of fruit names.
- A button is provided to print the currently selected item(s) from the Listbox.

This basic structure can be expanded with more complex functionalities like multiple selections, bindings to other events, and styling options. #Listbox Widget #TKinter #Python