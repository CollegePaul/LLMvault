### Image Display in Tkinter

Tkinter provides built-in support for displaying images using the `PhotoImage` class, which supports GIF and PPM/PGM formats natively. For other image formats such as JPEG or PNG, you can use the `PIL` (Python Imaging Library) module, specifically its submodule `ImageTk`, to convert these images into a format that Tkinter can understand.

Here’s how you can display an image in Tkinter:

1. **Using PhotoImage for GIF and PPM/PGM formats:**

```python
import tkinter as tk

# Create the main window
root = tk.Tk()
root.title("Displaying GIF Image")

# Load a GIF image
photo = tk.PhotoImage(file="example.gif")

# Create a label to display the image
label = tk.Label(root, image=photo)
label.pack()

# Run the application
root.mainloop()
```

2. **Using PIL (Pillow) for JPEG and PNG formats:**

First, ensure you have Pillow installed (`pip install pillow`), then use `ImageTk.PhotoImage`.

```python
from tkinter import Tk, Label
from PIL import Image, ImageTk

# Create the main window
root = Tk()
root.title("Displaying JPEG Image")

# Load a JPEG image using PIL
image = Image.open("example.jpg")
photo = ImageTk.PhotoImage(image)

# Create a label to display the image
label = Label(root, image=photo)
label.pack()

# Run the application
root.mainloop()
```

In both examples, an `Image` object is created and then converted into a format that Tkinter can use via the `PhotoImage` or `ImageTk.PhotoImage` class. The `Label` widget is used to display the image.

Remember to replace `"example.gif"` or `"example.jpg"` with the path to your actual image file.

#Image Display #TKinter #Python