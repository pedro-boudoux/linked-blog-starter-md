**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:**

## Basic Concepts

- Links are fundamental to the internet's structure
- Without links, we'd need to type a different address for every page
- Links allow for website navigation and organization of content
- Links are important for search engines to index sites
- Links can connect to other pages or resources (like images)

## Link Structure

- Created using the `<a>` element (anchor tag)
- Requires the `href` attribute to specify destination
- General syntax: `<a href="destination">Link Text</a>`
- Link text is what users see and click on, not the actual URL

## Types of Links

1. **Absolute Links**
    
    - Used for external resources (other websites)
    - Include full URL with scheme (http/https)
    - Example: `<a href="https://example.com">Example Site</a>`
2. **Relative Links**
    
    - Used for internal pages within the same website
    - Don't need full domain, just filename or path
    - Example: `<a href="page.html">Another Page</a>`
    - For files in subfolders: `<a href="folder/page.html">Page in Folder</a>`

## Link Appearance

- Links typically appear blue when unvisited
- Change to purple after being visited
- Usually underlined by default

## Website Structure

- Websites are collections of HTML files organized in folders
- URLs (Uniform Resource Locators) are used to reference files
- Simple relative URL example: `vintagecookbooks.html`
- Image example: `<img src="images/nfld.jpg" alt="Picture of Newfoundland">`

## Practical Example

```html
<h1>Favourite Nordic Baking Books</h1>
<ul>
  <li>"Scandinavian Baking" by Trine Hahnemann</li>
  <li><a href="https://ca.phaidon.com/store/food-cook/the-nordic-baking-book-9780714876849/">
    The Nordic Baking Book</a> by Magnus Nilsson</li>
  <li>"Meyer's Bakery" by Claus Meyer</li>
</ul>
```
