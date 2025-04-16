**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:**
# Embedding Images in HTML

## `<img>` Tag Basics
-   Used to insert images into a webpage.
-   Image content is defined externally (via a URL).
-   Self-closing tag (no separate closing tag).
-   Basic syntax: `<img src="path/to/image.jpg" alt="Image description">`

### Attributes
-   `src` (required): Specifies the URL (location and filename) of the image.
-   `alt` (required): Provides alternative text for the image, enhancing accessibility for:
    -   Search engines
    -   Screen readers
    -   Situations where the image cannot be displayed.

## Image Dimensions
-   By default, images are displayed at their native resolution.
-   Optional attributes to control dimensions:
    -   `height`: Specifies the image height in pixels.
    -   `width`: Specifies the image width in pixels.
-   Setting only one dimension will scale the image proportionally.
-   Setting both dimensions may distort (stretch) the image.
-   **Best Practice:** Use CSS to control image dimensions for better flexibility, especially with media queries for responsive design.

```html
<img src="cortado.jpg" width="104" height="142">
```

## Text Alternatives (`alt` Attribute)
- Crucial for accessibility and SEO.
- Provides a textual description of the image content.
- Used by:
    - Screen readers for visually impaired users.
    - Text-only browsers.
    - Search engine crawlers to understand the image content.

```html
<img src="cortado.jpg" alt="Spanish coffee" width="104" height="142">
```

## Example: Adding Images to a Book List
- The example demonstrates adding book cover images to a list of favorite baking books.
- The `<img>` tag with the `src` attribute pointing to the image file and the `height` attribute set to `200` is included within each list item (`<li>`).

### HTML Structure
```html
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>BAKING</title>
  </head>
  <body>
    <h1>Favourite Baking Books</h1>
    <p>What makes a baking book a favourite? Choosing cookbooks in general is
    somewhat of a personal preference. Usually we are drawn towards a few
    recipes, ones that stand out or books that have a story. Baking is
    a little different because it is a quasi-science that requires accurate
    measuring, time watching, and following a recipe precisely. In some cases
    these books have few is any pictures, others offer step-by-step visuals
    for complicated bakes. The books below inspire my baking:
  </p>
  <ul>
    <li>"P&acirc;tisserie at Home" by M&eacute;lanie Dupuis <br>
      <img src="patisserieathome.jpg" height="200">
    </li>
    <li>"Modern Baking" by Donna Hay <br>
      <img src="modernbaking.jpg" height="200">
    </li>
    <li>"The Nordic Baking Book" by Magnuss Nilsson <br>
      <img src="nordicbaking.jpg" height="200"> <br>
    </li>
    </ul>
  </body>
  
  </html>
```

### Expected Output
- A webpage titled "Favourite Baking Books".
- A paragraph explaining the criteria for favorite baking books.
- An unordered list of three baking books.
- Each list item includes the book title and author, followed by an image of the book cover with a set height of 200 pixels.

