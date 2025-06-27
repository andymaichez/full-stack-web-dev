#  HTML Text Formatting

HTML provides a variety of tags to structure and format text content on web pages. These tags help define the meaning, emphasis, or style of text.

---

##  Headings (`<h1>` to `<h6>`)

Used for defining headings of different levels.  
- `<h1>` is the **most important** (main heading)  
- `<h6>` is the **least important**

**Good Practice**: Use only **one `<h1>`** per page for SEO and accessibility.

```html
<h1>This is a Main Heading</h1>
<h2>This is a Sub-Heading</h2>
<h3>This is a Sub-Sub-Heading</h3>
```

---

##  Paragraphs (`<p>`)

Used for regular blocks of text.  
Each `<p>` tag creates a new paragraph with some space above and below it by default.

```html
<p>This is the first paragraph of text on my webpage.</p>
<p>And this is the second paragraph. It contains more information.</p>
```

---

##  Line Break (`<br>`)

Inserts a single line break inside a paragraph without starting a new one.  
**Self-closing tag**

```html
<p>This line will break here.<br>And continue on the next line.</p>
```

---

## ➖ Horizontal Rule (`<hr>`)

Creates a horizontal line, often used to separate content sections.  
**Self-closing tag**

```html
<p>Content above the line.</p>
<hr>
<p>Content below the line.</p>
```

---

## Bold Text (`<strong>` and `<b>`)

- `<strong>`: Semantically indicates strong importance. Text is typically **bold**.
- `<b>`: Bold text for presentation only.

```html
<p>This is <strong>important</strong> information.</p>
<p>This is <b>just bold</b> text.</p>
```

---

## _Italic Text_ (`<em>` and `<i>`)

- `<em>`: Emphasizes the text. Typically shown in *italics*. (Semantic)
- `<i>`: Italic text for stylistic purposes, not necessarily important. (Presentational)

```html
<p>I really <em>love</em> HTML!</p>
<p>The term <i>carpe diem</i> means "seize the day."</p>
```

---

##  Marked Text (`<mark>`)

Highlights text as if using a highlighter pen.

```html
<p>Please remember to <mark>save your work</mark>.</p>
```

---

## Small Text (`<small>`)

Represents fine print or side comments, like copyright notices.

```html
<p><small>&copy; 2025 My Awesome Website. All rights reserved.</small></p>
```

---

## Superscript (`<sup>`) and Subscript (`<sub>`)

- `<sup>`: Displays text **above** the normal line (e.g., exponents).
- `<sub>`: Displays text **below** the normal line (e.g., chemical formulas).

```html
<p>The formula for water is H<sub>2</sub>O.</p>
<p>E=mc<sup>2</sup> is Einstein's famous equation.</p>
```

---

##  Best Practices

- Use semantic tags like `<strong>` and `<em>` instead of `<b>` and `<i>` when meaning is important.
- Avoid using `<br>` excessively; prefer proper paragraphing.
- Don’t overuse `<mark>` unless really necessary—it can distract users.

---

##  Practice Time

Create a text-based webpage that includes:

- Headings from `<h1>` to `<h3>`
- At least two paragraphs
- One line break and one horizontal rule
- Examples of bold and italic text using both semantic and presentational tags
- Highlighted and small text
- One superscript and one subscript
