**Class:** [[Web Design and Development]]
**Date:** 14-04-2025
**Topics:** [[Intermediate HTML]]


# Creating Tables in HTML

Tables are very useful for displaying different types of information, and they aren’t that hard to create in HTML. An HTML table is defined using the `<table>` tag.

Each table row is defined with the `<tr>` tag. A table header is defined using the `<th>` tag. By default, table headings are bold and centred. A table data/cell is defined with the `<td>` tag. Here is an example which puts information on a series of books in table form:

```html
<table>
    <tr>
        <th>Title</th>
        <th>Author</th>
        <th>ISBN</th>
    </tr>
    <tr>
        <td>The Great British Book of Baking</td>
        <td>Linda Collister</td>
        <td>978-0718157111</td>
    </tr>
    <tr>
        <td>British Baking</td>
        <td>Oliver Peyton</td>
        <td>978-0224086615</td>
    </tr>
    <tr>
        <td>Great British Bakes</td>
        <td>Mary-Anne Boermans</td>
        <td>978-0224095563</td>
    </tr>
</table>
```

The `<td>` elements are the data containers of the table. They can contain HTML elements, such as: text, images, lists, other tables, etc. For example, the above table, when rendered, looks like this:

## CSS Modification of Tables

By default, tables are displayed without borders. This default can be modified by changing the CSS style for tables. The style change below adds a border around the table, headings, and data:

```css
table, th, td {
    border: 1px solid black;
}
```

To get rid of the “double” borders, add the collapse property:

```css
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
}
```

It is also possible to add some padding around the data in the cells to make them more visually appealing.

```css
th, td {
    padding: 10px;
}
```

It is also possible to align the headings using the `text-align` property:

```css
th {
    text-align: left;
}
```

Or, maybe add some border-spacing around the entire table:

```css
table {
    border-spacing: 10px;
}
```
