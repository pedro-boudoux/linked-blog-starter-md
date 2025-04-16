**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Basics of CSS]]

### Styling Text
- Styling text is crucial for readability, as webpages often contain significant amounts of textual content.
- The most fundamental text style is **colour**, controlled by the `color` property.
    ```css
    p {
      color: blue; /* Sets the text colour of all paragraph elements to blue */
    }
    ```
    - Text colours can be specified using CSS colour names (e.g., `blue`), RGB values (e.g., `rgb(0, 0, 255)`), or HEX values (e.g., `#0000FF`).

- **Text Alignment:** The `text-align` property sets the horizontal alignment of text within an element. Possible values are `left`, `right`, `center`, and `justify`.
    ```css
    p {
      color: blue;
      text-align: left; /* Aligns the paragraph text to the left (default) */
    }
    ```
    
- **Other Text Styles:**
    - `text-decoration`: Adds decorations to text, such as `overline`, `line-through`, `underline`, or `none` (removes decorations).
    - `text-transform`: Modifies the case of text (`uppercase`, `lowercase`, `capitalize`).
    - `text-indent`: Indents the first line of text within an element.
    - `line-height`: Sets the vertical space between lines of text.
    - `word-spacing`: Adjusts the horizontal space between words.

### Fonts
- Fonts significantly impact the visual appeal and readability of a website.
- CSS font properties define the font family, boldness, size, and style of text.
- CSS defines two types of font families:
    - **Generic Families:** Groups of fonts with similar characteristics (e.g., `serif`, `sans-serif`, `monospace`, `cursive`, `fantasy`).
    - **Font Families:** Specific font names (e.g., `Times New Roman`, `Arial`, `Verdana`).
- The `font-family` property specifies a prioritized list of fonts (a "fallback" system). The browser will use the first available font in the list.
    ```css
    p {
      font-family: Verdana, Arial, sans-serif; /* Tries Verdana, then Arial, then any sans-serif font */
    }
    ```
    
- `font-size`: Controls the size of the font. Can be set using absolute units (e.g., `px`) or relative units (e.g., `em`).
    - **Pixels (`px`):** An absolute unit.

        ```css
        p {
          font-family: Verdana, Arial, sans-serif;
          font-size: 12px;
        }
        ```
        
    - **`em` units:** Relative to the font size of the parent element. The default browser font size is typically 16px, so `1em` = `16px`.

        ```css
        p {
          font-family: Verdana, Arial, sans-serif;
          font-size: 0.75em; /* Equivalent to 12px if the parent's font size is 16px */
        }
        ```
        
- **Other Font Styles:**
    - `font-style`: Sets the text to italic (`italic`) or normal (`normal`).
    - `font-weight`: Specifies the boldness of the text (`bold`, `normal`, or numeric values like `400` for normal and `700` for bold).
    - `font-variant`: Allows displaying text in small capital letters (`small-caps` or `normal`).

**Example CSS:**

```css
body {
  background-color: lightcyan;
}

p {
  margin: 20px;
  color: blue;
  text-align: justify; /* Justifies the paragraph text */
  width: 75%;
}

h1 {
  font-family: Verdana, Arial, sans-serif; /* Sets the font for h1 headings */
  color: orange; /* Sets the text colour of h1 headings to orange */
  border-style: dotted;
  border-width: 2px;
  border-color: Tomato;
  padding: 10px;
  margin-left: 20px;
  width: 75%;
}
```

This CSS will style the `body` background, paragraph text (colour, alignment, margin, width), and `h1` headings (font family, colour, border, padding, margin, width). The `h1` heading will use the Verdana font (or Arial, or a default sans-serif font if the others are not available) and will be orange. The paragraph text will be blue and justified within a 75% width container.