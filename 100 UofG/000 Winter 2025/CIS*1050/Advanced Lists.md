**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]

## List Markers

How can we modify how lists appear? One way is modifying the list item marker. This can be done for both ordered and unordered lists. For unordered lists, the default marker is a bullet (solid circle), but it can also be modified to a circle, square, or nothing, using a CSS inline style change called `list-style-type`. Consider this example from Unit 3:

```html
<!DOCTYPE html>     
<html lang="en">       
	<head>         
		<meta charset="utf-8" />         
		<title>A Basic Web Page</title>       
	</head>       
	<body>         
		<h1>Favourite Baking Books</h1>         
		<ul>           
			<li>"Patisserie at Home" by Melanie Dupuis</li>
			<li>"Modern Baking" by Donna Hay</li>
			<li>"Scandinavian Baking" by Trine Hahnemann</li>
		</ul>
</body>  
</html>   
```

We can modify this by modifying the first line of the unordered list `<ul>` to:

`<ul style="list-style-type:square;">`

For ordered lists the type attribute can be used to change the list item marker to one of the following: `type="1"`, numbers; `type="A"`, uppercase letters; `type="a"`, lowercase letters; `type="I"`, uppercase Roman numerals; and `type="i"`, lowercase Roman numerals. We can use this to modify the code above to use an ordered list with lowercase Roman numerals as list item markers:

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8"/>
		<title>A Basic Web Page</title>
	</head>
<body>
	<h1>Favourite Baking Books</h1>
	<ol type="i">
		<li>"Patisserie at Home" by Melanie Dupuis</li>
		<li>"Modern Baking" by Donna Hay</li>
		<li>"Scandinavian Baking" by Trine Hahnemann</li>
	</ol>
</body>
</html>   
```

## Description Lists

Another type of list is the description list, which has a list of terms, with a description of each term. It uses tags that are a little different from ordered and unordered lists. The `<dl>` tag defines the description list, the `<dt>` tag defines the term (name), and the `<dd>` tag describes each term. Here is an example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <title>A Basic Web Page</title>
</head>
<body>
    <h1>Styles of Espresso</h1>
    <dl>
        <dt><strong>Lungo</strong></dt>
        <dd>- 1½ fl oz with crema</dd>

        <dt><strong>Espresso</strong></dt>
        <dd>- 1 fl oz with crema</dd>

        <dt><strong>Ristretto</strong></dt>
        <dd>- ½ fl oz with crema</dd>

        <dt><strong>Long black</strong></dt>
        <dd>- espresso poured into hot water</dd>

        <dt><strong>Americano</strong></dt>
        <dd>- espresso with water added last</dd>
    </dl>
</body>
</html>

```

## List Counting

By default, a list will start counting at 1, which may not always be what is required. This can be modified using the `start` attribute, for example, to start an ordered list at number 42:

`<ol start="42">`

It is even possible to combine several attributes, for example:

```html
<ol start="42" type="i">
	<li>"The Great British Book of Baking" by Linda Collister</li>
	<li>"British Baking" by Oliver Peyton</li>
	<li>"Great British Bakes" by Mary-Anne Boermans</li>
</ol>
```