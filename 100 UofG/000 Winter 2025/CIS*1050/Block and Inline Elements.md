**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]

## Blocks
*Block* is a display type for an HTML element. Every element has a display type by default, usually *block* or *inline*, here are some elements which are displayed as a block by default:

- `<div>`
- `<footer>`
- `<section>`
- `<article>`
- `<header>`
- `<video>`

## Inline
*Inline* elements don't start on a new line and only take up as much width as necessary. Examples of some inline by default elements:

- `<span>`
- `<a>`
- `<img>`
- `<br>`

## Divisions
Divisions (`<div>`), is a block element which defines a division or section in a HTML document. Often used as a container for other elements and stuff;
```html
<div> 
	<!-- div content goes here -->
<div/>
```

## Classes
Used to classify elements (duh) and gives elements with the same class common characteristics.

Giving an element a class in HTML:
```html title="Giving an element a class (HTML)"
<div class="generic">
	<!-- Content -->
<div/>
```

Adding characteristics to a class in CSS:
```css title="Adding characteristics to a class in CSS"
.generic {
	color: green;
	display: flex;
	flex-direction: column;
	/* and more!!! */
}
```

## IDs
*IDs* give elements unique identifiers so that they can be easily accessed and manipulated by *css* or *javascript* without having to waste time with annoying selectors.

```html title="Giving an element an ID"
<a id="idName" href="google.ca"> Google <a/>
```

```css title="Styling an element with id"
#idName {
	color: red;
	/* etc */
}
```

