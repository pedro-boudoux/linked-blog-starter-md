**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Basics of CSS]]
### CSS Box Model
- In CSS, every HTML element is treated as a **box**.
- The **CSS Box Model** describes the rectangular boxes that are generated for elements in the document tree and laid out according to the visual formatting model.
- The box model consists of several layers that surround the actual content of an HTML element:
    
    1. **Content:** The actual text, images, or other HTML elements within the box. The `width` and `height` properties apply to the content area.
    2. **Padding:** The space around the content, inside the border. Controlled by the `padding` properties (`padding-top`, `padding-right`, `padding-bottom`, `padding-left`, and the shorthand `padding`). The background of the element extends into the padding area.
    3. **Border:** A line that surrounds the padding and content. Controlled by the `border` properties (`border-width`, `border-style`, `border-color`, and the shorthand `border`).
    4. **Margin:** The transparent space outside the border, used to create space between elements. Controlled by the `margin` properties (`margin-top`, `margin-right`, `margin-bottom`, `margin-left`, and the shorthand `margin`).

- The box model enables us to:
    - Add borders around elements.
    - Define spacing between elements using margins.
    - Create space around the content within an element using padding.

**Example:**

```css
p {
  width: 75%; /* Sets the width of the content area to 75% of its parent */
  margin: 20px; /* Adds a 20px margin on all four sides of the paragraph */
  border: 5px solid Tomato; /* Creates a 5px solid Tomato-colored border around the padding and content */
  padding: 10px; /* Adds a 10px padding on all four sides between the content and the border */
  color: blue; /* Sets the text color of the content to blue */
}
```

In this example, for each `<p>` element:

- The **content** area will have a width of 75% of its containing element.
- There will be a **padding** of 10 pixels around the text content.
- A solid **border** with a width of 5 pixels and the colour Tomato will surround the padding.
- A **margin** of 20 pixels will be applied to all sides of the border, creating space between this paragraph and any adjacent elements.
- The text within the paragraph will be blue (this is a content style, not part of the box model dimensions).
