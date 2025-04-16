**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Basics of CSS]]

### CSS Style Sheets

- When a browser reads a CSS sheet, it formats the associated HTML document according to the styles specified.
- There are three main ways to apply CSS:
    - Inline styles (within HTML elements).
    - Internal style sheets (within the `<style>` tags in the `<head>` of an HTML document).
    - External style sheets (separate `.css` files linked to HTML documents).

### External Style Sheet

- **Benefit:** Allows for modifying the look of an entire website by changing a single `.css` file. Similar to changing a "theme."
- External stylesheets are plaintext files with a `.css` extension, ideally located in the same folder as the HTML files.
- Each HTML page needs to link to the external stylesheet using the `<link>` element within the `<head>` section.

```html title=HTML
<!DOCTYPE html>
  <html lang=”en”>
    <head>
      <meta charset=”utf-8” />
      <title>BAKING</title>
      <link rel="stylesheet" type="text/css" href="style-1.css">
    </head>
    <body>
      <h1>The Art of Cookery (1774)</h1>
      <h3><em>To make a pound cake.</em></h3>
      <p>
        TAKE a pound of butter, beat it in an earthen pan with your
        hand one way, till it is line a fine thick cream, then have ready
        twelve eggs, but half the whites; beat them well, and beat
        them up with the butterm a pound of flour beat in it, a pound
        of sugar, and a few carraways. Beat it all well together for
        an hour with your hand, or a great wooden spoon, butter a pan
        and put it in, and then bake it an hour in a quick oven.
      </p>
    </body>
  </html>
```

```css title=CSS
p {
	color: red;
}
```

- The `.css` file (`style-1.css` in this example) contains CSS rules that define the styling of HTML elements.
- The `<link>` tag attributes:
    - `rel="stylesheet"`: Specifies the relationship between the linked document and the current document (it's a stylesheet).
    - `type="text/css"`: Indicates the type of the linked document (CSS).
    - `href="style-1.css"`: Specifies the URL or path to the CSS file.

### Internal Style Sheet

- Used when a single HTML page has unique styling requirements.
- Internal styles are defined within the `<style>` and `</style>` tags, placed inside the `<head>` section of the HTML page.

```html
<!DOCTYPE html>
  <html lang=”en”>
    <head>
      <meta charset=”utf-8” />
      <title>BAKING</title>
      <style>
        p {color: red;}
      </style>
    </head>
    <body>
      <h1>The Art of Cookery (1774)</h1>
      <h3><em>To make a pound cake.</em></h3>
      <p>
        TAKE a pound of butter, beat it in an earthen pan with your hand one way, till it is line a fine thick cream, then have ready twelve eggs, but half the whites; beat them well, and beat them up with the butterm a pound of flour beat in it, a pound of sugar, and a few carraways. Beat it all well together for an hour with your hand, or a great wooden spoon, butter a pan and put it in, and then bake it an hour in a quick oven.
      </p>
    </body>
  </html>
```
- The CSS rules are directly embedded within the HTML document.

### Output of Both Examples
A rendering of the HTML code above, with h1 and h3 headings, and paragraph text in red.

- Both the external and internal style sheet examples will result in the same visual output in the browser, where the text within the `<p>` tags is displayed in red.

