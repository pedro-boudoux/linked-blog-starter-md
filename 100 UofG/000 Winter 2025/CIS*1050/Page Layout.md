**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS Page Layout and Positioning

## Position Property Types

The `position` property defines how an element is positioned on the page:

- **static**: Default setting where elements appear in normal document flow
- **absolute**: Takes element out of normal flow and positions it relative to its nearest positioned ancestor
    - Can be placed anywhere using `top`, `right`, `bottom`, and `left` properties
- **relative**: Similar to static, but can be offset from original position
    - Uses `top`, `right`, `bottom`, and `left` for positioning
- **fixed**: Similar to absolute but positioned relative to the browser window
    - Stays in place when page is scrolled

## Two-Column Layout with Absolute Positioning

### CSS Example:

```css
nav.navbar {
  position: absolute;
  top: 0;
  left: 0;
  width: 180px;
}

.content {
  margin-left: 180px;
}
```

### HTML Structure:

```html
<nav class="navbar">
  <!-- Navigation content -->
</nav>

<article class="content">
  <!-- Main content -->
</article>
```

### Limitations:

- Difficult to determine where absolutely positioned elements end
- Challenging to position other elements around these boxes
- Works best for pages with small navigation and large content areas

## Float Positioning

Float shifts an element to the left or right, allowing other content to flow around it.

### CSS Example:

```css
nav.navbar {
  float: left;
  width: 180px;
}

.content {
  margin: 180px;
}
```

### Controlling Content Flow with Clear

The `clear` property prevents elements from wrapping around floated elements:

- `clear: left` - Clears left floating boxes
- `clear: right` - Clears right floating boxes
- `clear: both` - Clears both left and right floating boxes

### Adding a Footer Below Floated Content:

```css
nav.navbar {
  float: left;
  width: 180px;
}

.content {
  margin: 180px;
}  

#footer {
  clear: both;
}
```

## Practical Example: Modified Navigation Bar

Converting an inline navigation menu to a vertical sidebar:

```css
nav.navbar {
  float: left;
  width: 150px;
}

nav.navbar li {
  display: block;
}

nav.navbar li a {
  padding: 5px 7px;
  margin: 2px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  width: 100px;
}
```

This creates a fixed-width vertical navigation menu on the left side of the page with the main content flowing to its right.