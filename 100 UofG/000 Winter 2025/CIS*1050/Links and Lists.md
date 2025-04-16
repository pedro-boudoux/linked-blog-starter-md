**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Basics of CSS]]

## Links

### Basic Styling
- Links (`<a>`) can be styled like any other element:
    
    ```css
    a {
      color: deeppink;
    }
    ```
    
### Link States
- Pseudo-classes allow for state-based styling:
    
    - `a:link` – unvisited
        
    - `a:visited` – visited
        
    - `a:hover` – mouse over
        
    - `a:active` – clicked
        
    ```css
    a:link    { color: deepskyblue; }
    a:visited { color: deeppink; }
    a:hover   { color: magenta; }
    a:active  { color: gold; }
    ```
    
### Background Highlighting

- Add `background-color` to emphasize links:
    ```css
    a:link {
      color: deepskyblue;
      background-color: cyan;
    }
    ```
    
### Styled Link Button

- Combine multiple styles for a button-like link:
    
    ```css
    a:link, a:visited {
      background-color: Tomato;
      color: white;
      padding: 5px 7px;
      text-align: center;
      text-decoration: none;
      display: inline-block;
    }
    
    a:hover, a:active {
      background-color: red;
    }
    ```
    
## Lists

### Basic Marker Style
- Customize bullets or numbers:

    ```css
    ul { list-style-type: square; }
    ol { list-style-type: lower-roman; }
    ```
    

### Image Markers
- Use an image instead of default bullets:
    
    ```css
    ul { list-style-image: url('book-icon.jpg'); }
    ```
    

### Marker Position
- `list-style-position: inside | outside`:
    
    ```css
    ul { list-style-position: inside; }
    ```
    
### Background Colors

- Style entire list or individual items:
    
    ```css
    ul {
      background: bisque;
      padding: 20px;
    }
    ul li {
      background: paleturquoise;
    }
    ```
