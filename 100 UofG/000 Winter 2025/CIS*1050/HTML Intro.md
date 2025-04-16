
**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** #html

# HTML FAQs

## Why is it called HyperText?

hypertext refers to the ability to click links and navigate between interconnected documents on the web. html pages can pull in other resources (css, images, video, scripts), combining them into a single browser-rendered page.

## Who invented html?

Tim Berners-Lee at CERN in the 90s. based it on SGML. created http to fetch docs via hyperlinks. this kicked off the modern web. HTML has since evolved:

- *html 2* (nov 1995)  
- *html 3.2* (jan 1997)  
- *html 4.0* (dec 1997)  
- *html 4.01* (dec 1999)  
- *html5* (oct 2014)  

## how is an html document recognized?

by file extension: `.htm` or `.html`. other dynamic files (.php, .asp, etc) output html too—just generated server-side. browser doesn’t care, it just renders html.

## what is html5?

current html standard (w3c). adds multimedia support (e.g. `<video>`), semantic tags (`<nav>`, `<header>`, `<article>`), and better structure. flash used to dominate rich content, but apple ditched it with iphone. html5 + css + js took over.

## what is a markup language?

a human-readable way to annotate content so that machines (like browsers) can process/display it. uses special tags, e.g. `<tag>`.

## what are tags?

tags are angle-bracketed markers that define html elements. most come in pairs: opening `<tag>` and closing `</tag>`. content goes in between. browsers parse these and render the result.

## what are attributes?

attributes go in the opening tag to provide extra info. structure: `name="value"`. e.g.:

```html
<a href="https://eatingwildfood.ca">Foody Website</a>
```

here, `href` is an attribute on the `<a>` tag, defining the link destination.