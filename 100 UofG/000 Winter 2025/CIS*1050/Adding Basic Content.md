**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[HTML Intro]]

# Adding Basic Content

## Page Titles

- set with `<title>` inside `<head>`
- appears in browser tab and search engine results

*example*:
```html
<title>A Basic Web Page</title>
```

## Paragraphs
- `<p>` creates a paragraph of text
- must be inside `<body>`

*example*:
```html
<p> Hello bro hello bro </p>
```

## Headings
- use `<h1>` to `<h6>` for hierarchical structure
- `<h1>` is largest/most important, `<h6>` least
- defines structure for both users and search engines

*example*:
```html
<h1> Hello this is a heading </h1>
```

## Lists
### Unordered List 
- bullet-pointed
- use when order doesn't matter

*example*: 
```html
<ul>
  <li>"Patisserie at Home" by Melanie Dupuis</li>
  <li>"Modern Baking" by Donna Hay</li>
  <li>"Scandinavian Baking" by Trine Hahnemann</li>
</ul>
```

### Ordered List
- Numbered Items
- Use for sequences or prioritization

```html
<ol>
  <li>"Patisserie at Home" by Melanie Dupuis</li>
  <li>"Modern Baking" by Donna Hay</li>
  <li>"Scandinavian Baking" by Trine Hahnemann</li>
</ol>
```

### Nested List
- list within a list to group info hierarchically
- use `<ul>` or `<ol>` inside a parent list's `<li>`

*example*:
```html
<ul>
  <li>Nordic</li>
    <ol>
      <li>"Scandinavian Baking" by Trine Hahnemann</li>
      <li>"The Nordic Baking Book" by Magnus Nilsson</li>
      <li>"Meyer's Bakery" by Claus Meyer</li>
    </ol>
  <li>British</li>
    <ol>
      <li>"The Great British Book of Baking" by Linda Collister</li>
      <li>"British Baking" by Oliver Peyton</li>
      <li>"Great British Bakes" by Mary-Anne Boermans</li>
    </ol>
</ul>
```

## HTML Rules
- `<ul>` can only contain `<li>` children (same with `<ol>`)
- semantic meaning of ordered vs unordered is significant
