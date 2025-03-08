### Understanding <img> in Web Development

The `<img>` tag is fundamental in web development for embedding images on web pages. This HTML element allows developers to incorporate visual content, enhancing the user experience by adding graphics, logos, charts, and more.

**Attributes of the <img> Tag:**
- **src**: Specifies the path to the image file.
- **alt**: Provides alternative text if the image cannot be displayed. It is also important for accessibility.
- **width** and **height**: Define the dimensions of the image in pixels or other units.
- **title**: Offers additional information about the image when hovered over.

**Basic Example:**
```html
<img src="logo.png" alt="Company Logo" width="200" height="150">
```

In this example, an image named `logo.png` is displayed with dimensions of 200x150 pixels. The text "Company Logo" serves as alternative content if the image fails to load.

**CSS for Styling Images:**
Styling images using CSS can significantly enhance their appearance and functionality on a website.
```css
img {
    border-radius: 8px; /* Rounds the corners of the image */
    box-shadow: 2px 2px 5px grey; /* Adds a shadow to the image for depth */
}
```

**JavaScript for Image Manipulation:**
JavaScript can be used to dynamically change images, such as swapping them out or applying effects.
```javascript
// Change an image source on click
document.getElementById('image').addEventListener('click', function() {
    this.src = 'new-image.png';
});
```
In the above JavaScript snippet, clicking on the image with id `image` will replace it with `new-image.png`.

#Img #Web