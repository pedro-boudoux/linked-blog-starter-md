**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS Selectors: Classes and IDs

## Overview

- CSS selectors can be integrated into external CSS files instead of using inline styles
- This approach reduces clutter in HTML documents

## Class Selectors

- Denoted by a period/full stop (`.`) before the name
- Example:
    
    ```css
    .butterfly {  background-color: lightcyan;  color: orangered;  margin: 20px;  padding: 20px;}
    ```
    
- Can be applied to multiple elements in HTML

## ID Selectors

- Denoted by a hash character (`#`) before the name
- Example:
    
    ```css
    #flutterby {  background-color: lightcyan;  color: orangered;  margin: 20px;  padding: 20px;}
    ```
    
- Should be unique within an HTML document (used for single elements)

## Benefits

- Keeps HTML cleaner and more readable
- Separates content (HTML) from presentation (CSS)
- Makes styling more manageable and consistent