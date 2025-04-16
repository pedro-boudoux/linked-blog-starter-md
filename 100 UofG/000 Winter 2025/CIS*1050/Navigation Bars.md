**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS Navigation Bars

## Basic Structure

Navigation bars start with basic HTML, typically using unordered lists:

```html
<ul>
  <li><a href="#home">Home</a></li>
  <li><a href="nordic-books.html">Nordic</a></li>
  <li><a href="british-books.html">British</a></li>
  <li><a href="french-books.html">French</a></li>
</ul>
```

## Styling Process

### Step 1: Remove Default List Styling

Remove bullets, margins, and padding:

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

### Step 2: Style List Items

For basic structure, style the list items as blocks:

```css
li {
  display: block;
}
```

### Step 3: Style Links for Vertical Navigation

Format the anchor elements within list items:

```css
li a {
  display: block;
  width: 100px;
}
```

This makes the entire area clickable and sets a fixed width.

### Step 4: Add Visual Styling

Add colors, alignment, padding, and font styling:

```css
li a {
  display: block;
  width: 100px;
  color: Tomato;
  text-align: left;
  padding: 20px;
  text-decoration: none;
  font-family: 'Oswald', sans-serif;
}
```

### Step 5: Add Interactive Elements

Add hover effects to improve user experience:

```css
li a:hover {
  opacity: 0.7;
}
```

Alternative hover styling:

```css
li a:hover {
  background-color: #555;
  color: white;  
}
```

## Creating Horizontal Navigation Bars

Convert the vertical menu to horizontal by changing the display property:

```css
li {
  display: inline-block;
}
```

This removes line breaks between items, placing them side by side.

## Key CSS Properties Used

- `list-style-type`: Removes bullets
- `margin` and `padding`: Control spacing
- `display`: Controls how elements are rendered (block, inline-block)
- `width`: Sets element width
- `color`: Text color
- `text-align`: Horizontal alignment
- `text-decoration`: Controls underlines
- `font-family`: Sets typeface
- `opacity`: Controls transparency
- `background-color`: Sets background color

## Complete CSS

```css
/* Reset list styling */
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

/* Basic styling for all list items */
li {
  display: block;
}

/* Styling for links inside list items - Vertical navigation */
li a {
  display: block;
  width: 100px;
  color: Tomato;
  text-align: left;
  padding: 20px;
  text-decoration: none;
  font-family: 'Oswald', sans-serif;
}

/* Hover effect */
li a:hover {
  background-color: #555;
  color: white;
}

```

