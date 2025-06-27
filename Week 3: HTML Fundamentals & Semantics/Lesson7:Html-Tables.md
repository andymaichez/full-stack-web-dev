# HTML Tables

HTML tables are used to **display tabular data** — data that fits into rows and columns.  
Tables are **not meant** for creating page layouts. Use CSS for layout instead.

---

## Basic Table Tags

| Tag        | Purpose                                            |
|------------|----------------------------------------------------|
| `<table>`  | Wraps the entire table                             |
| `<thead>`  | (Optional) Contains the table header row(s)        |
| `<tbody>`  | Contains the main body rows of the table           |
| `<tfoot>`  | (Optional) Contains the table footer row(s)        |
| `<tr>`     | Defines a **table row**                            |
| `<th>`     | Defines a **header cell** (bold and centered)      |
| `<td>`     | Defines a **standard data cell**                   |

---

## Basic Table Structure

```html
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>City</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Alice</td>
            <td>30</td>
            <td>New York</td>
        </tr>
        <tr>
            <td>Bob</td>
            <td>24</td>
            <td>London</td>
        </tr>
        <tr>
            <td>Charlie</td>
            <td>35</td>
            <td>Paris</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">Data last updated: June 2025</td>
        </tr>
    </tfoot>
</table>
````

---

## Key Attributes

### `colspan`

* Merges multiple columns into one cell
* `colspan="number"`

### `rowspan`

* Merges multiple rows into one cell
* `rowspan="number"`

---

## Example: `colspan` and `rowspan`

```html
<table>
    <thead>
        <tr>
            <th colspan="2">Student Information</th>
            <th rowspan="2">Grade</th>
        </tr>
        <tr>
            <th>Name</th>
            <th>ID</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Emily</td>
            <td>S101</td>
            <td>A</td>
        </tr>
        <tr>
            <td>David</td>
            <td>S102</td>
            <td>B+</td>
        </tr>
    </tbody>
</table>
```

---

## Styling Tables 

HTML supports attributes like `border` and `cellpadding`, but these are **deprecated** in modern development.
Use **CSS** for presentation (CSS Recommended).

```html
<table border="1" cellpadding="10">
    <!-- Not best practice — use CSS instead -->
</table>
```

---

## Best Practices

* Always use `<thead>`, `<tbody>`, and `<tfoot>` for clear structure.
* Use `colspan` and `rowspan` sparingly for clarity.
* Avoid using tables for layout — that’s what CSS is for!

---

## Exercise: Creating a Simple Table

1. Open your `index.html` file.
2. Add a new section titled **"Monthly Budget"** or **"Product Catalog"**.
3. Create a table with:

   * At least **3 columns** and **4–5 rows**
   * Use `<thead>` for column headers
   * Use `<tbody>` for the data
4. Include a `colspan` or `rowspan` somewhere in the table (e.g., summary row).
5. Save and view the file in your browser.


We'll enhance the look of tables using CSS later!
