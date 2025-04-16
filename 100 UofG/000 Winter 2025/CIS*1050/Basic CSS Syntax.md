**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Basics of CSS]]

### Basic CSS Syntax

- A CSS rule-set consists of a **selector** and a **declaration block**.
- The **selector** targets the HTML element(s) to be styled.
- The **declaration block** is enclosed in curly braces `{}` and contains one or more **declarations**, separated by semicolons `;`.
- Each **declaration** consists of a1 **CSS property** and its **value**, separated by a colon `:`.

CSS

```css
h1 {
   color: red;
   font-size: 16px;
}
```

- **CSS Comments:** Start with `/*` and end with `*/`.

### CSS Selectors

- Used to target HTML elements for styling.
    
    - **Element Selector:** Selects elements based on their tag name.
        ```css
        p {color: red;} /* Styles all paragraph elements */
        ```

    - **ID Selector:** Selects a single, unique element based on its `id` attribute. Uses a hash symbol `#` followed by the `id` value.
        ```css
        #parat {color: red;} /* Styles the element with id="parat" */
        ```

    - **Class Selector:** Selects elements with a specific `class` attribute. Uses a period `.` followed by the class name.

    - **Grouping Selector:** Applies the same styles to multiple selectors, separated by commas.
        ```
        h1, h2, p {color: red;} /* Styles all h1, h2, and p elements */
        ```


### Colours

- CSS offers several ways to specify colours:
    
    - **Colour Names:** Predefined keywords (e.g., `Tomato`, `LightCyan`, `Blue`). CSS has 140 standard colour names.
    - **RGB:** Specifies colour using the red, green, and blue components (values from 0 to 255).
        
        ```css
        p {
          color: RGB(21,135,214);
        }
        ```
        
    - **HEX:** Uses hexadecimal values to represent colours (e.g., `#1587D6`).
    - **HSL:** Defines colour using hue (0-360), saturation (0%-100%), and lightness (0%-100%).
        
        ```css
        /* Example */
        HSL(205, 90%, 46%);
        ```
        
    - **RGBA:** RGB with an alpha channel to specify opacity (0.0 - fully transparent, 1.0 - fully opaque).
    - **HSLA:** HSL with an alpha channel for opacity.
	- **Colour-Related CSS Properties:**
    
    - `background-color`: Sets the background colour of an element.

        ```css
        body {
          background-color: LightCyan;
        }
        ```
        
    - `color`: Sets the text colour of an element.

        ```css
        p {
          color: Blue;
        }
        ```
        
    - `border-color`: Sets the colour of an element's border.

        ```css
        p {
          border: 2px solid Blue;
        }
        ```
        

### Backgrounds

- CSS allows setting background images and controlling their properties.
    - `background-image`: Specifies an image to be used as the background.

        ```css
        body {
          background-image: url(“baking.jpg”);
        }
        ```
        
    - `background-repeat`: Controls how the background image is repeated (`repeat`, `repeat-x`, `repeat-y`, `no-repeat`).

        ```css
        body {
          background-image: url(“baking.jpg”);
          background-repeat: repeat-x;
        }
        ```
        
    - `background-position`: Sets the starting position of the background image (`top`, `bottom`, `left`, `right`, `center`, or pixel/percentage values).

        ```css
        body {
          background-image: url(“baking.jpg”);
          background-repeat: no-repeat;
          background-position: bottom;
        }
        ```
        
    - `background-attachment`: Determines if the background image scrolls with the page or is fixed (`fixed`, `scroll`).

        ```css
        body {
          background-image: url(“baking.jpg”);
          background-repeat: no-repeat;
          background-position: bottom;
          background-attachment: fixed;
        }
        ```
        
    - **Shorthand `background` property:** Allows setting multiple background properties in one declaration. The order of values is: `background-color`, `background-image`, `background-repeat`, `background-attachment`, `background-position`.

        ```css
        body {
          background: url("baking.jpg") no-repeat fixed bottom;
        }
        ```
        
    - `background-size`: Specifies the size of the background image (`length`, `percentage`, `cover`, `contain`). `cover` resizes the image to cover the entire container.

        ```css
        body {
          background-image: url(“baking.jpg”);
          background-size: cover;
        }
        ```
        

### Borders

- CSS border properties control the style, width, and colour of an element's border.
    - `border-style`: Defines the appearance of the border (`solid`, `dashed`, `dotted`, etc.).

        ```css
        h1 {
          border-style: dotted;
        }
        ```
        
    - `border-width`: Sets the thickness of the border (in `px`, `pt`, `cm`, `em`, or using predefined values like `thin`, `medium`, `thick`). Can have 1-4 values for different sides.

        ```css
        h1 {
          border-style: dotted;
          border-width: 2px;
        }
        ```
        
    - `border-color`: Sets the colour of the border. Can have 1-4 values for different sides.

        ```css
        h1 {
          border-style: dotted;
          border-width: 2px;
          border-color: Tomato;
        }
        ```
        
    - **Shorthand `border` property:** Sets `border-width`, `border-style`, and `border-color` in one declaration.

        ```css
        h1 {
          border: 2px dotted Tomato;
        }
        ```
        
    - `border-radius`: Creates rounded corners.

### Margins

- CSS margin properties create space around elements (outside the border).
    - `margin-top`, `margin-bottom`, `margin-right`, `margin-left`: Set margins for individual sides.
    - Values can be `auto`, `percentage`, or `length` (`px`, `pt`, `cm`, `em`).
    - `auto` horizontally centers block-level elements.
    - **Shorthand `margin` property:** Can take 1-4 values to set all or individual margins (top, right, bottom, left).

        ```css
        body {
          margin: 20px; /* All sides */
        }
        ```
        

### Padding

- CSS padding property creates space within an element (inside the border).
    - `padding-top`, `padding-bottom`, `padding-right`, `padding-left`: Set padding for individual sides.
    - Uses `length` and `percentage` values.
    - **Shorthand `padding` property:** Similar to `margin`, can take 1-4 values.

        ```css
        h1 {
          padding: 10px; /* All sides */
        }
        ```
        

### Height and Width

- `height` and `width` properties set the dimensions of an element.
    - Values can be `auto` (browser calculates), `length`, or `percentage` of the containing block.

        ```css
        h1 {
          width: 75%;
        }
        ```
        

### An Example Style Sheet (`styleit.css`)

```css
body {
  background-color: lightcyan;
}

p {
  color: blue;
  margin-left: 20px;
}

h1 {
  color: orange;
  border-style: dotted;
  border-width: 2px;
  border-color: Tomato;
  padding: 10px;
  margin-left: 20px;
  width: 75%;
}
```

This style sheet would result in a webpage with a light cyan background, blue paragraph text with a 20px left margin, and orange `h1` headings with a dotted tomato-coloured border, 10px padding, a 20px left margin, and a width of 75% of the browser window.