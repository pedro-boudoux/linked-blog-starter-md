**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]

- `<header>`: a header for a document, or section
- `<nav>`: a container for navigation links
- `<section>`: a section in a document
- `<article>`: an independent “self-contained” article
- `<aside>`: content to one side of the main content, (e.g., sidebar)
- `<footer>`: a footer for a document or section
- `<details>`: additional things
- `<summary>`: a header for the `<details>` element

## Articles and Sections
*Article* elements can be used to mark a standalone section of the content, like for a blog post for example. 
*Section* elements, can be used to split up articles.

Example:
```html
<body>

	<article>
	
		<section id=”preamble”>
		
			<p>[Introduction, historical context etc.]</p>
			
		</section>
		
		<section id=”ingredients”>
		
			<p>[Ingredients required]</p>
			
		</section>
		
		<section id=”instructions”>
		
			<p>[How to cook/bake]</p>
			
		</section>
		
	</article>

</body> 
```

## Headers and Footers
Both *headers* and *footers* provide special *self-descriptive* sections.

## Asides
An *aside* is used to represent content that is related to the content surrounding it.

## Navigation
A *nav* element is used to mark up a group of navigation links.

## Figures
*Figures* are used to mark up and label *figures* in an article.

```html
<body>
<article>
  <section id=”preamble”>
    <p>[Introduction, historical context etc.]</p>
    <figure>
      <img src="gingerbread.jpg">
      <figcaption>A German gingerbread</figcaption>
    </figure>
  </section>
</article>
</body> 
```

