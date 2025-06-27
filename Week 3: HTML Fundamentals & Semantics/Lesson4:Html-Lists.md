#  HTML Lists

Lists are fundamental for organizing information in a clear and readable way. HTML provides **three types of lists**:

- Unordered Lists (`<ul>`)
- Ordered Lists (`<ol>`)
- Description Lists (`<dl>`)

---

##  Unordered Lists (`<ul>`)

Used for lists of items where **order doesn’t matter**.  
Each list item is marked with a **bullet point** by default.

- List items are defined using the `<li>` (list item) tag.

```html
<h3>My Favorite Fruits:</h3>
<ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Oranges</li>
    <li>Grapes</li>
</ul>
```

---

##  Ordered Lists (`<ol>`)

Used for lists where **order matters** (e.g., steps, rankings).  
Each item is numbered or labeled automatically.

- List items also use the `<li>` tag.

```html
<h3>Steps to Make Coffee:</h3>
<ol>
    <li>Boil water.</li>
    <li>Add coffee grounds to filter.</li>
    <li>Pour hot water over grounds.</li>
    <li>Enjoy your coffee!</li>
</ol>
```

###  `type` Attribute for `<ol>`

You can change the numbering format using the `type` attribute:

| Type | Output Example     |
|------|---------------------|
| `1`  | 1, 2, 3 (default)   |
| `a`  | a, b, c             |
| `A`  | A, B, C             |
| `i`  | i, ii, iii          |
| `I`  | I, II, III          |

```html
<ol type="A">
    <li>First item</li>
    <li>Second item</li>
</ol>
```

---

##  Description Lists (`<dl>`)

Used for pairs of **terms and their descriptions** (like a dictionary or glossary).

- `<dl>`: Starts the description list
- `<dt>`: Defines the term
- `<dd>`: Defines the description

```html
<h3>Glossary of Web Terms:</h3>
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language. The standard language for creating web pages.</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets. Used for styling the look and feel of web pages.</dd>

    <dt>JavaScript</dt>
    <dd>A programming language that enables interactive web pages.</dd>
</dl>
```

---

##  Nested Lists

You can nest one list inside another to create **hierarchical structures**.

 Place nested lists inside a `<li>` item of the parent list.

```html
<h3>My To-Do List:</h3>
<ul>
    <li>Grocery Shopping
        <ul>
            <li>Milk</li>
            <li>Eggs</li>
            <li>Bread</li>
        </ul>
    </li>
    <li>Work Tasks
        <ol>
            <li>Finish report</li>
            <li>Email client</li>
            <li>Schedule meeting</li>
        </ol>
    </li>
    <li>Personal Errands</li>
</ul>
```

---

##  Best Practices

- Use unordered lists for items without sequence.
- Use ordered lists for step-by-step instructions or rankings.
- Use description lists for glossaries, FAQs, or term explanations.
- Indent nested lists properly for clarity and structure.

---

##  Exercise : Creating Various Lists

In your `index.html` file, try the following:

1. Add a section titled **"My Favorite Hobbies"** using an **unordered list**.
2. Create a section **"Top 3 Movies"** using an **ordered list**. Try using `type="i"` or `type="A"`.
3. Make a small **FAQ** section using a **description list** with 2–3 Q&A items.
4. Nest another list inside one of the items above.
5. Save your file and open it in the browser to view results.
