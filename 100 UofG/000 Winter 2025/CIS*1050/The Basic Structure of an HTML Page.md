**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[HTML Intro]]

# basic structure of an html page

## minimal layout

basic skeleton of an html5 page:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
  </head>
  <body>
    <!-- content goes here -->
  </body>
</html>
```

## explanation

- `<!DOCTYPE html>`: tells the browser this is html5.

- `<html>`: wraps entire page. includes a lang attribute (e.g. "en").

- `<head>`: holds metadata (title, charset, stylesheets, etc.).

- `<meta charset="utf-8">`: defines character encoding so symbols display properly. no closing tag.

- `<body>`: contains visible content—text, images, links, etc.

- `<!-- comment -->`: used for notes in code, ignored by browser.

## notes
- nested tags should be indented (e.g. 2 spaces) for readability.
- keep this layout as a reusable boilerplate for new pages.
- without anything in `<body>`, browser will render a blank page.

