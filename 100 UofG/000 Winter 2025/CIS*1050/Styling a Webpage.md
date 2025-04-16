**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:**

# inline elements, styling, and html character entities

## inline vs block elements
- **block elements** (e.g. `<p>`, `<div>`) take up full width and stack vertically  
- **inline elements** (e.g. `<em>`, `<strong>`) affect content *within* a line

## inline styling examples
```html
<p>
  <em>Photography takes an instant out of time, altering life by holding it still.</em>
  - <strong>Dorothea Lange</strong>
</p>
```

- `<em>`: italicizes text, semantically means "emphasis"
- `<strong>`: bolds text, semantically means "strong importance"
- inline elements only modify the text they wrap—not the whole line

## nesting inline elements
- you can nest `<strong>` inside `<em>` or vice versa
  - emphasizes layered significance

## line breaks
- use `<br>` for a hard line break
  - renders a newline in output
  - don't abuse it just to add space
```html
<em>Some text</em><br>
<strong>Author Name</strong>
```

- `<br>` and `<br />` are equivalent. pick a style and stick with it.

## inline css styles
- use `style="..."` to apply CSS directly in html elements
- example props:
  - `background-color`
  - `color`
  - `font-family`
  - `font-size`
  - `text-align`

```html
<p style="color:red; font-family:courier; font-size:160%; text-align:center;">
  Styled paragraph
</p>
```

- not ideal for scalability—use external CSS for big projects

## html entities (special characters)
- used for symbols that are reserved or unavailable on keyboard
- format: `&name;` or `&#number;`

### common reserved characters
| character | entity | decimal |
|----------|--------|---------|
| `<`      | `&lt;` | `&#60;` |
| `>`      | `&gt;` | `&#62;` |
| `&`      | `&amp;`| `&#38;` |

### curly quotes
- `&ldquo;` = “  
- `&rdquo;` = ”  
- `&lsquo;` = ‘  
- `&rsquo;` = ’  

## utf-8 and special chars
- add to `<head>`:  
```html
<meta charset="utf-8" />
```

- prevents rendering issues with chars like `ä`, `é`, etc.

### example:
```html
<p>"P&acirc;tisserie at Home" by M&eacute;lanie Dupuis</p>
```

### selected special character entities:
| symbol | entity | decimal |
|--------|--------|---------|
| ©      | `&copy;` | `&#169;` |
| °      | `&deg;`  | `&#186;` |
| ™      | `&trade;`| `&#8482;` |
| é      | `&eacute;` | `&#233;` |
| â      | `&acirc;`  | `&#226;` |
| ×      | `&times;`  | `&#215;` |
| ±      | `&plusmn;` | `&#177;` |

