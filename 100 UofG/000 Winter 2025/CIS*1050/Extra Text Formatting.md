**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]


## Abbreviations

The tag `abbr` is used to mark up an abbreviation, which is a shortened form of a word or phrase. The expanded phrase that the abbreviation represents can be defined in the value of the title attribute. Here is an example:

```html
<abbr title="HyperText Markup Language">HTML</abbr>
```

## Quotations

The `blockquote` and `q` tags are used for quotations. The `blockquote` tag is generally used for standalone often multi-line quotations, whereas `q` is used for in-line quotations. If the source of a quotation is found on the web, then the `cite` attribute can be used to point to the source. Here is an example of an inline quote:

```html
<p>Naturalist Sir David Attenborough has said that with respect to climate change we face <q>irreversible damage to the natural world and the collapse of our societies</q>. </p>
```

Here’s a further example of a blockquote:

```html
<blockquote cite="https://metro.co.uk/2019/01/30/story-destroyed-world-plastic-fix-8405293/">
<p>"Every breath of air we take, every mouthful of food that we take, comes from the natural world. And if we damage the natural world, we damage ourselves."
Sir David Attenborough discussion with Prince William at the World Economic Forum, Davos, 2019</p>
</blockquote>
```

## Citations

There is also a `cite` tag. This tag can be used to define the title of a piece of work. It marks the text in italic. For example:

```html
<p>Jamie Oliver’s new book is titled <cite>Jamie Cooks Italy</cite>. </p>
```

## Code

Representing computer code in the wrong font can make it look weird (i.e., code not written in a monospaced font like Courier looks odd). One way around this is to use the `code` tag for inline code. Here is an example of a small program:

```html
<p>A C program typically uses the term <code> void </code> to imply nothing, or emptiness. </p>
```

This would be rendered as:

A C program typically uses the term `void` to imply nothing or emptiness.

There is also the tags `samp` to display sample output and `kbd` for user input (short for keyboard). Larger pieces of code can be placed verbatim (with all white spaces intact) using the `pre` tag.

```html
<pre><code>
#include <stdio.h>
int main(void)
{
    printf("Hello World!
");
    return 0;
}
</code></pre>
```

The resulting code would look like this:

A rendering of code using the `pre` tag.

A rendering of code using the `<pre>` tag.

## Addresses

The `address` tag is used for writing contact details for an entire website. Here is an example:

```html
<h3>Contact details</h3>
<address>
<ul>
    <li>text details</li>
    <li>email@address</li>
    <li>web-address details</li>
</ul>
</address>
```

This renders as a rendering of a list of address details.
