# Legend for Normalization 3NF

There are no code fence blocks or other standard for rendering entities in the three stages to third-normal-form. However, in Markdown, you can add styles to indicate such things as primary keys and foreign keys.

## Legend

his legend is a guide to reading and interpreting the table listings under 0NF through 3NF.

> **TableName:** - Table names will be bolded and end with a colon. (e.g.: `**TableName:**`)

> (Column, Names) - Column names for a table will be enclosed in (rounded parenthesis).

> <b class="pk">PrimaryKeyFields</b> - Primary key fields will be bold and inside a box. (e.g: `<b class="pk">PrimaryKeyFields</b>`)

> <u class="fk">ForeignKeyFields</u> - Foreign key fields will be a wavy underline in italic and green. (e.g.: `<u class="fk">ForeignKeyFields</u>`)

> <b class="gp">{</b>Repeating Groups<b class="gp">}</b> - Groups of repeating fields will be identified in 0NF stage, and will be enclosed in orange curly braces. (e.g.: `<b class="gp">{</b>Repeating, Group, Fields<b class="gp">}</b>`)

To make this legend appear correctly in MarkDown, include the following style markup at the end of your markdown file:

```html
<style type="text/css">
.pk {
    font-weight: bold;
    display: inline-block;
    border: solid thin blue;
    padding: 0 1px;
}
.fk {
    color: green;
    font-style: italic;
    text-decoration: wavy underline green;    
}
.gr {
    color: darkorange;
    font-size: 1.2em;
    font-weight: bold;
}
</style>
```

## Demo

The following demo illustrates a 1st/2nd normal form stage development for the concept of a Purchase Order.

### 0NF

After performing Zero-Normal Form, a single table was generated: **Order**.

**Order:**	(<b class="pk">OrderNumber</b>, CustomerNumber, FirstName, LastName, Address, City, Province, PostalCode, Phone, Date, <b class="gr">{</b>ItemNumber, Description, Quantity, CurrentPrice, SellingPrice, Amount<b class="gr">}</b>, Subtotal, GST, Total)

### 1NF

After performing First-Normal Form, a new table was generated: OrderDetail.

**Order:**	(<b class="pk">OrderNumber</b>, CustomerNumber, FirstName, LastName, Address, City, Province, PostalCode, Phone, Date, Subtotal, GST, Total)

**OrderDetail:**	(<b class="pk"><u class="fk">OrderNumber</u>, ItemNumber</b>, Description, Quantity, CurrentPrice, SellingPrice, Amount)


----

<style type="text/css">
.pk {
    font-weight: bold;
    display: inline-block;
    border: solid thin blue;
    padding: 0 1px;
}
.fk {
    color: green;
    font-style: italic;
    text-decoration: wavy underline green;    
}
.gr {
    color: darkorange;
    font-size: 1.2em;
    font-weight: bold;
}
</style>