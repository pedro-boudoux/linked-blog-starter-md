**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate CSS]]

# CSS At-Rules (@Rules)

At-rules are special CSS instructions that encapsulate and apply CSS rules to specific contexts. They all begin with an "at" symbol (@).

## @import
Used to import other CSS files into the current stylesheet.
- Must be placed at the top of a stylesheet
- Helpful for breaking down complex CSS into manageable files

**Syntax:**

```css
@import url(someotherstyle.css);
```

## @media
Used to apply styles to specific media types and conditions.

### Media Types:

- `screen` (computers, tablets, mobile devices)
- `print` (printers)
- `projection`
- `handheld`
- `all` (default)

### Common Use: Responsive Web Design
Media queries deliver tailored stylesheets to different devices based on their characteristics.

**Basic Example:**

```css
body {
   background-color: lightskyblue;
}

@media screen and (min-width: 500px) { 
   body {
      background-color: lightcyan;
   }
}
```

In this example:
- Screens narrower than 500px get a light sky blue background
- Screens 500px or wider get a light cyan background

### Advanced Media Queries
Can target specific device characteristics:

```css
@media screen and (min-device-height: 2436px)
              and (max-device-width: 1125px) { 
   /* apply style */
}
```

Common applications:
- Creating responsive navigation menus (horizontal on large screens, vertical on small)
- Optimizing layout for different devices
- Adjusting font sizes for readability

## @font-face
Allows use of specialized fonts not installed on the user's system.

**Syntax:**

```css
@font-face { 
   font-family: "font of Tatooine";
   src: url(fontoftatooine.woff);
}
```

**Usage:**

```css
body { 
   font-family: "font of Tatooine", arial, sans-serif;
}
```

This will:
1. Download the specified font file from the same directory as the CSS
2. Apply it to the body of the webpage
3. Fall back to arial or sans-serif if the custom font fails to load