# Learn CSS Pseudo Selectors - Balance Sheet

## What I learnt

A small number of pseudo-selectors and further styling of tables.

### Tables

Table elements can use captions that describe what data the table holds, useful not only for typical users but also screen readers. Caption elements should **_always be the 1st child_** of a table.

|                   |                         |
| ----------------- | ----------------------- |
| `<thead></thead>` | Container table headers |
| `<tbody></tbody>` | Main table content      |
| `<tr></tr>`       | Table rows              |
| `<td><td>`        | Individual table cells  |
| `<th></th>`       | Cell headers            |

### Styling text for screen readers only.

Within the html there is a class of `sr-only` [30-32], [70], [84-86], [124], [138-140], [145]. Firstly text is wrapped within a `<span>` so that we can target separately.

styles.css [10] targets any span element with a class of `sr-only`.

`clip` defines the **_visible_** portions of an element.

`clip-path` determines the **_shape_** of the clip property [Don't really know what this means].

Need to understand why elements are given properties of `width: 1px` | `height: 1px` | `overflow: hidden` | `white-space: nowrap` | `position: absolute` | `padding: 0` | `margin: -1px`

styles.css [31-35] - By making the h1 container a flexbox we can swap the 2 <span> elements around (remember we will hide the text "AcmeWidgetCorp")

### :first-of-type pseudo-selector

Target the first element that matches the selector.

styles.css [37-39] Will select the first <span> element in the h1 .flex container index.html [14]

### :last-of-type pseudo-selector

This is the opposite of `:first-of-type`

### Styling of #years

styles.css [51-61] style the #years at the top of the table. at line [56] we use the calc function which calculates a value based on others. in this example we set the **_right_** padding to 25px (1.25rem + 2px) NOTE: Root font-size in this example is 20px so 1.25rem = 25px

Set the `z-index` to a high positive value to ensure this element isn't blocked by other content as we scroll.

styles.css [60-64] styles the text by aligning right (which adds space between the years). `span[class]` will target any <span> element that has a **_class attribute_**

## :not pseudo-selector

Targets elements that do not match the argument / selector. [70] selects all <span> elements that do not have a class of `.sr-only`

## Styling tables

`border-collapse: collapse` creates a single border rather than having a border around each cell

### table cells (tbody td)

The table would benefit from having fixed width cells. This can be achieved by setting min-width and max-width to the same values styles.css [94-98]

### table heading (tbody th)

styles.css [100-102] use the cal function to set the width of <th> to 100% of it's container - 12rem.

## attribute selector

styles.css [104-107]. Using the attribute selector `[attribute="value"]` we target elements that have an attribute with the same name as the "value" provided. In this case we select <tr> elements that have the class of `total`.

styles.css [109-112] targets <th> elements that are children of <tr> with a class of `total`

## Reflection

## References
