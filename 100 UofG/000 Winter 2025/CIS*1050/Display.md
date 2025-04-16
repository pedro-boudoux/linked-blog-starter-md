**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS Display Property

## Inline Display

The `display: inline` property displays elements as boxes that flow along the line of text.

- Follows the natural flow of a line
- Default display type for elements like anchors (`<a>`) and emphasis (`<em>`)
- Useful for making elements appear in a continuous horizontal flow
- Cannot manipulate height, width, or vertical margins effectively

**Example:**

```css
li {
  display: inline;
}
```

This would make list items appear side by side in a continuous line rather than each having its own line.

## Block Display

The `display: block` property creates standalone boxes that take up the full width available.

- Takes up entire width of containing element
- Creates line breaks before and after the element
- Allows manipulation of height, width, margins, and padding
- Default display type for elements like headings (`<h1>`) and paragraphs (`<p>`)

**Example:**

```css
li {
  display: block;
}
```

This would make each list item appear on its own line (which is actually the default behavior for list items).

## None Display

The `display: none` property completely removes the element from the rendered page.

- Element is not displayed at all
- Takes up no space in the layout
- Useful for toggling information on and off
- Different from `visibility: hidden` which hides the element but preserves its space

**Example:**

```css
.hidden-content {
  display: none;
}
```
