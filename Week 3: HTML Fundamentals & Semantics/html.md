# Introduction to HTML

## What is HTML?

**HTML** stands for **HyperText Markup Language**. It is the **standard language** used to create and structure content on the web.

You can think of HTML as the **skeleton of a webpage**—it lays out how things are arranged, what content appears, and gives structure to the elements that a browser will display.

---

###  Breaking Down the Term

- **HyperText**:  
  Refers to text that links to other text. It allows for the **interlinking of web pages** using hyperlinks.

- **Markup**:  
  Describes the use of tags to **annotate** content. For example:
  
  - `<h1>` marks text as a heading  
  - `<p>` marks text as a paragraph  
  - `<img>` embeds an image

- **Language**:  
  A set of **rules and syntax** that browsers can understand and interpret to display content on the web.

---

###  Key Concepts

- **HTML is NOT a Programming Language**  
  It doesn’t perform logic, loops, or decision-making.  
  Its primary role is to **structure content**.

- **Browsers Interpret HTML**  
  Web browsers (like Chrome, Firefox, or Safari) read HTML files and convert them into the **visual pages** we interact with.

- **Foundation of Every Webpage**  
  Behind every webpage is HTML. Whether it's a blog, a shop, or a social media platform, HTML provides the structural base.

---

### Example Analogy

> **HTML is like the blueprint of a house.**  
> - It specifies **where the walls, windows, and doors** go.  
> - **CSS** is like the **interior design**—it adds colors, fonts, and styles.  
> - **JavaScript** is like the **electricity and plumbing**—it adds interactivity and functionality.

---

# HTML Document Structure

Understanding the structure of an HTML document is fundamental to creating well-formed and valid web pages. Every HTML page follows a consistent format that tells the browser how to interpret and display the content.

---

## Basic HTML Structure

Here is a simple example of a complete HTML document:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My First HTML Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <p>This is my very first paragraph on a web page.</p>
  </body>
</html>
````

---

##  Breakdown of Each Part

### 1. `<!DOCTYPE html>`

* This is the **Document Type Declaration**.
* It tells the browser that this document follows **HTML5**, which is the latest version of HTML.
* This declaration is **not an HTML tag**, but a **directive to the browser**.
* It must appear **at the very top** of every HTML document.

---

### 2. `<html lang="en">`

* The `<html>` element is the **root** of the HTML document.
* All other tags are nested inside this tag.
* The `lang="en"` attribute specifies the **language** of the document (English in this case).

  * This helps with **screen readers**, **search engines**, and **browser behavior**.

---

### 3. `<head>`

The `<head>` element contains **metadata**—information about the document that is **not displayed** on the web page itself.

#### Common Elements Inside `<head>`:

* #### `<meta charset="UTF-8">`

  * Declares the **character encoding** used by the document.
  * UTF-8 supports most characters and symbols from all known languages.
  * Helps ensure emojis, special characters, and international text display correctly.

* #### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

  * Makes the page **responsive**.
  * Tells the browser to **scale the content** properly on different devices (especially mobile).

* #### `<title>My First HTML Page</title>`

  * Defines the **title** of the page shown in the browser tab.
  * Important for **SEO** and **user navigation**.

* #### Other Elements That Can Be Included:

  * `<link>` – Links to external files like CSS stylesheets.
  * `<script>` – Links to or contains JavaScript code.
  * `<style>` – Embeds internal CSS styles.

---

### 4. `<body>`

* The `<body>` element contains everything that will be **visible in the browser window**.
* This is where you place all **visual content**:
  Headings, paragraphs, images, links, tables, forms, and more.

#### Example:

```html
<body>
  <h1>Hello, World!</h1>
  <p>This is my very first paragraph on a web page.</p>
</body>
```

---

##  Summary

| Element            | Purpose                                               |
| ------------------ | ----------------------------------------------------- |
| `<!DOCTYPE html>`  | Declares the document type and HTML version           |
| `<html lang="en">` | Root element; sets document language                  |
| `<head>`           | Holds metadata like title, character set, and links   |
| `<meta>`           | Provides metadata like encoding and viewport settings |
| `<title>`          | Sets the browser tab title                            |
| `<body>`           | Contains visible content of the page                  |

---

#  HTML Tags & Attributes (Deep Dive)

##  What is a Tag?

HTML is made up of **tags**, which are instructions to the browser that define how content should appear or behave.

- Most HTML tags come in **pairs**:
  - **Opening tag**: `<tagname>`
  - **Closing tag**: `</tagname>`
  - **Content**: What’s inside the tags

**Example:**

```html
<p>This is a paragraph.</p>
```

- `<p>` is the opening tag
- `</p>` is the closing tag
- `"This is a paragraph."` is the content

---

##  Self-Closing (Empty) Tags

Some tags don’t wrap around any content, so they don’t have closing tags. These are called **empty** or **self-closing** tags.

**Common Examples:**

| Tag       | Purpose                         |
|-----------|----------------------------------|
| `<br>`    | Line break                      |
| `<hr>`    | Horizontal rule (divider line)  |
| `<img>`   | Display an image                |
| `<input>` | Form input field                |
| `<meta>`  | Metadata for the HTML document  |
| `<link>`  | Link to external CSS file       |

*In HTML5, you don’t need a forward slash like `<br />`, but it’s okay if you include it.*

---

##  Attributes in HTML

**Attributes** provide extra information about elements.

- Always placed inside the **opening tag**
- Usually follow a **name="value"** format

**Syntax:**

```html
<tagname attribute="value">Content</tagname>
```

---

##  Common HTML Attributes

| Attribute | Purpose |
|----------|---------|
| `id`     | Assigns a **unique identifier** to the element. Used in CSS and JavaScript |
| `class`  | Groups elements for styling or behavior. Multiple elements can share the same class |
| `style`  | Adds inline CSS styling (not recommended for large projects) |
| `title`  | Adds a tooltip that appears on hover |
| `alt`    | Describes an image (for accessibility and SEO) |
| `src`    | Specifies the **source** URL of media (images, audio, video, etc.) |
| `href`   | Specifies a **link target** for `<a>` and `<link>` elements |
| `target` | Defines where to open the linked document (e.g., `_blank` opens in new tab) |
| `type`   | Specifies the type of input, script, or media |
| `value`  | Sets the value of inputs like `<input>` and `<option>` |
| `name`   | Names a form input (used when submitting form data) |
| `placeholder` | Adds a hint inside an input box |
| `disabled` | Disables an element |
| `readonly` | Makes an input uneditable but visible |

---

##  Examples

###  Basic Attribute Example

```html
<h1 id="page-title" class="main-heading" style="color: green;" title="Welcome to our site">
  My Website Title
</h1>
```

- `id="page-title"` → uniquely identifies this heading
- `class="main-heading"` → groups it with other main headings
- `style="color: green;"` → colors the text green
- `title="..."` → shows a tooltip on hover

---

###  Image with Attributes

```html
<img src="profile.jpg" alt="Portrait of a smiling person" width="200" height="200">
```

- `src` → specifies the image file to display
- `alt` → used by screen readers or when image fails to load
- `width` and `height` → dimensions in pixels

---

###  Anchor (Link) Tag with Attributes

```html
<a href="https://example.com" target="_blank" title="Visit Example Site">Visit Site</a>
```

- `href` → the link URL
- `target="_blank"` → opens the link in a new tab
- `title` → shows a tooltip on hover

---

##  Real-Life Analogy

Imagine HTML tags like **containers** or **instructions** in a recipe:

- Tags are the **containers/instructions**
- Attributes are the **details** or **customizations**

Example:  
```html
<button style="background: blue;" disabled>Click Me</button>
```
This is like saying:  
> “Create a button with a blue background, but don’t let the user click it.”

---

##  Best Practices

- Always quote attribute values:  `class="example"`, not  `class=example`
- Use `id` for **unique elements**, `class` for **reusable styles**
- Use semantic tags (e.g., `<header>`, `<main>`, `<article>`) over generic `<div>` when appropriate
- Keep inline styles (`style="..."`) minimal—prefer external CSS
- Always include the `alt` attribute in images for accessibility

---

##  Practice Time

Create a simple webpage that includes:

- A heading with `id`, `class`, and `style` attributes
- A paragraph with a tooltip using `title`
- A clickable link that opens in a new tab
- An image with `src`, `alt`, and `width`
- A self-closing `<hr>` and `<br>`

---
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

---
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

---

# HTML Links

Links (hyperlinks) are what connect web pages together, forming the "web."  
They allow users to navigate from one page to another — both **within the same website** and to **external websites**.

---

##  Anchor Tag (`<a>`)

The `<a>` tag is used to create hyperlinks.

- The most important attribute is `href` (Hypertext REFerence), which specifies the destination URL.

```html
<a href="https://www.google.com">Visit Google</a>
````

---

## Types of Links

### External Links

* Links to **other websites**
* Use **absolute URLs** (include `http://` or `https://`)

```html
<p>Learn more about HTML on <a href="https://developer.mozilla.org/en-US/docs/Web/HTML">MDN Web Docs</a>.</p>
```

---

###  Internal Links

* Links to **other pages within the same website**
* Use **relative paths**

Example 1 — Same folder:

```html
<p>Go to the <a href="about.html">About Us</a> page.</p>
```

Example 2 — Subfolder:

```html
<p>Check out our <a href="pages/products.html">Products</a>.</p>
```

Example 3 — Going up a folder:

```html
<p>Go back to the <a href="../index.html">Homepage</a>.</p>
```

---

##  Opening Links in a New Tab

Use `target="_blank"` to open a link in a **new tab or window**.

```html
<p>Search the web with <a href="https://www.bing.com" target="_blank">Bing</a>.</p>
```

---

##  Image as a Link

Wrap an `<img>` tag inside an `<a>` tag to make it clickable.

```html
<a href="https://www.nasa.gov">
    <img src="nasa-logo.png" alt="NASA Logo">
</a>
```

---

##  Mailto Links

Creates a link that opens the user’s **default email app**.

```html
<p>Contact us at <a href="mailto:info@example.com">info@example.com</a>.</p>
```

---

##  Phone Links (for Mobile)

Allows mobile users to dial a number directly.

```html
<p>Call us: <a href="tel:+1234567890">+1 (234) 567-890</a></p>
```

---

##  Anchor Links (Bookmarks)

Link to a **specific section on the same page**.

1. Give the target element an `id`.
2. Use `href="#id"` in the link.

```html
<nav>
    <a href="#section1">Go to Section 1</a> |
    <a href="#section2">Go to Section 2</a>
</nav>

<h2 id="section1">Section 1: Introduction</h2>
<p>This is the content of section 1.</p>

<h2 id="section2">Section 2: Conclusion</h2>
<p>This is the content of section 2.</p>
```

---

##  Best Practices

* Use `target="_blank"` for external links so users don’t leave your site.
* Always provide descriptive anchor text (avoid “click here”).
* Use anchor links for **table of contents**, **navigation**, or **long documents**.
* Always test internal link paths in your folder structure.

---

## Exercise: Adding Links to Your Page

1. Create a new file named `about.html` in the same folder as `index.html`.

   * Add a basic structure, a heading like **"About Us"**, and a short paragraph.

2. In `index.html`, add:

   *  A link to `about.html`.
   *  An external link to your favorite site (open in new tab).
   *  A `mailto:` link with your email address.

3. *(Optional)*:

   * Add an `id` to one of your `<h2>` elements.
   * Add a link at the top that jumps to that section.

4. Save both files and test all your links!

---

#  HTML Images

Images are essential for making web pages visually appealing and informative.  
HTML provides the `<img>` tag to embed images into web pages.

---

##  The `<img>` Tag

- It is a **self-closing** tag (does not have a closing tag).
- Requires at least **two essential attributes**: `src` and `alt`.

```html
<img src="path/to/your/image.jpg" alt="Description of the image">
````

---

##  `src` Attribute (Source)

* Specifies the **path** or **URL** of the image file.

###  Relative Paths (Recommended for local images)

```html
<img src="images/logo.png" alt="Company logo">
```

###  Absolute Paths (For external images)

```html
<img src="https://example.com/banner.jpg" alt="Promotional banner">
```

---

## `alt` Attribute (Alternative Text)

* Crucial for **accessibility** and **SEO**
* Displays if the image cannot be loaded.
* Used by **screen readers** for visually impaired users.
* Helps search engines understand image content.

### Examples:

* Good: `alt="A red apple sitting on a wooden table"`
* Poor: `alt="apple"`

---

##  `width` and `height` Attributes

* Define the **size** of the image in pixels.
* Help avoid layout shifts during page load.
* For **responsive design**, CSS is generally preferred.

```html
<img src="flower.jpg" alt="Close-up of a red rose" width="300" height="200">
```

If you set **only one** (e.g., `width`), the browser automatically scales the other to maintain aspect ratio.

---

## Common Image File Formats

| Format           | Use Case                                         | Notes                       |
| ---------------- | ------------------------------------------------ | --------------------------- |
| `.jpg` / `.jpeg` | Photos and colorful images                       | Lossy compression           |
| `.png`           | Transparent or sharp-edged images (icons, logos) | Lossless compression        |
| `.gif`           | Simple animations, small icons                   | Limited to 256 colors       |
| `.webp`          | Modern alternative to JPG/PNG                    | Smaller size, good quality  |
| `.svg`           | Logos, icons, illustrations                      | Scalable without pixelation |

---

## Image as a Link

You can wrap an image inside an anchor (`<a>`) tag:

```html
<a href="https://example.com">
    <img src="logo.png" alt="Company Logo">
</a>
```

---

## Best Practices

* Always include descriptive `alt` text.
* Organize images in an `images/` subfolder.
* Use appropriate file formats for performance and quality.
* Avoid stretching by respecting the image’s aspect ratio.

---

## Exercise:  Embedding Images

1. Download or find a small image file (e.g., from **Unsplash** or **Pexels**).
2. Save it in a folder named `images` inside your project folder.
3. In `index.html`, add an `<img>` tag to display the image.
4. Include a descriptive `alt` attribute.
5. Try using `width` and `height` attributes.
6. *(Optional)*: Make the image a clickable link to an external site.
7. Save and open your page in a browser to view the result.

---
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

---

We'll enhance the look of tables using CSS later!

---
# HTML Forms

HTML forms are used to **collect user input** — essential for things like logins, searches, surveys, file uploads, and more.

---

## The `<form>` Tag

Defines a form for user input.

### Attributes:

- `action`: The URL to send the form data to.
- `method`: The HTTP method used to send the data:
  - `get`: Data appears in the URL (good for bookmarks, not for sensitive info).
  - `post`: Data is sent in the request body (better for sensitive/large data).

```html
<form action="/submit_form.php" method="post">
    <!-- Form fields go here -->
</form>
```

---

## Input Fields (`<input>`)

A versatile tag used for various types of input.  
It’s **self-closing** and usually includes:

- `type`: Specifies the type of input.
- `name`: A unique identifier for the data (used by the server).
- `value`: Optional. Initial/default value.

### Common Input Types

#### `text`
```html
<input type="text" id="username" name="username" placeholder="Enter your username">
```

#### `password`
```html
<input type="password" id="password" name="password" placeholder="Enter your password">
```

#### `email`
```html
<input type="email" id="email" name="email" placeholder="you@example.com">
```

#### `number`
```html
<input type="number" id="age" name="age" min="1" max="120">
```

#### `date`
```html
<input type="date" id="dob" name="dob">
```

#### `checkbox`
```html
<input type="checkbox" id="newsletter" name="newsletter" value="yes">
<label for="newsletter">Sign up for newsletter</label>
```

#### `radio`
Radio buttons must share the same `name` to work as a group.
```html
<input type="radio" id="male" name="gender" value="male">
<label for="male">Male</label><br>

<input type="radio" id="female" name="gender" value="female">
<label for="female">Female</label>
```

#### `file`
```html
<input type="file" id="resume" name="resume">
```

#### `submit` and `reset`
```html
<input type="submit" value="Submit Form">
<input type="reset" value="Clear Form">
```

---

## The `<label>` Tag

Improves accessibility. Use `for` to link to the input's `id`.

```html
<label for="firstName">First Name:</label>
<input type="text" id="firstName" name="firstName">
```

---

## The `<textarea>` Tag

Allows for multi-line text input. Use `rows` and `cols` to control size.

```html
<label for="comments">Comments:</label><br>
<textarea id="comments" name="comments" rows="5" cols="40"></textarea>
```

---

## The `<select>` Dropdown

Wrap `<option>` elements inside `<select>`.

```html
<label for="country">Country:</label>
<select id="country" name="country">
    <option value="usa">United States</option>
    <option value="can">Canada</option>
    <option value="uk" selected>United Kingdom</option>
    <option value="aus">Australia</option>
</select>
```

---

## The `<button>` Tag

More flexible than `<input type="submit">`.

```html
<button type="submit">Send Message</button>
<button type="button">Click Me!</button>
```

---

## Additional Attributes

- `placeholder`: Shows a hint inside input fields.
- `required`: Makes a field mandatory before submission.

```html
<input type="text" placeholder="Your Full Name" required>
```

---

## Exercise: Building a Simple Contact Form

1. In your `index.html`, add a new **"Contact Us"** section.
2. Create a `<form>` with `action="#"` and `method="get"`.
3. Add the following:
   - Text input for **Name**
   - Email input for **Email**
   - Textarea for **Message**
   - Radio buttons for **Preferred Contact Method** (Email, Phone)
   - Checkbox for **Subscribe to Newsletter**
   - Submit button
4. Add `placeholder` for all input fields.
5. Make **Name** and **Email** fields `required`.
6. Save and test the form (try submitting with required fields empty).



You’ve now learned how to create rich, accessible forms with HTML!

---
# Semantic HTML

Semantic HTML refers to the use of HTML5 elements that **clearly describe their meaning** in a human- and machine-readable way.  
This makes your code more readable, accessible, and better for SEO.

---

## Before Semantic Tags (Non-Semantic)

Developers used many `<div>` and `<span>` tags with `class` or `id` to describe content structure.

```html
<div id="header">...</div>
<div id="nav">...</div>
<div id="main-content">...</div>
<div id="footer">...</div>
```

---

## With Semantic Tags

Semantic HTML5 elements replace non-semantic wrappers with meaningful tags.

```html
<header>...</header>
<nav>...</nav>
<main>...</main>
<article>...</article>
<aside>...</aside>
<footer>...</footer>
```

---

## Common Semantic Elements

| Tag | Purpose |
|-----|---------|
| `<header>` | Introductory content or navigational links |
| `<nav>` | Primary navigation links |
| `<main>` | The main content of the document |
| `<section>` | A standalone section (with a heading) |
| `<article>` | A self-contained composition (blog post, article) |
| `<aside>` | Sidebar or content related to the main content |
| `<footer>` | Footer content (author, copyright, links) |
| `<figure>` | Groups media content (like images) |
| `<figcaption>` | Caption for a figure |
| `<mark>` | Highlights text |
| `<time>` | Represents time or date |

---

## Example Layout Using Semantic Tags

```html
<body>
  <header>
    <h1>My Blog</h1>
  </header>

  <nav>
    <a href="index.html">Home</a> |
    <a href="about.html">About</a>
  </nav>

  <main>
    <article>
      <h2>First Blog Post</h2>
      <p>Published on <time datetime="2025-06-27">June 27, 2025</time></p>
      <p>This is the content of the blog post.</p>
    </article>

    <aside>
      <h3>Related Links</h3>
      <ul>
        <li><a href="#">HTML5 Overview</a></li>
        <li><a href="#">Accessibility Tips</a></li>
      </ul>
    </aside>
  </main>

  <footer>
    <p>&copy; 2025 My Blog. All rights reserved.</p>
  </footer>
</body>
```

---

## Benefits of Semantic HTML

- Improves **accessibility** for screen readers
- Helps **SEO** understand your page structure
- Easier to **maintain and read** code
- Makes content more **meaningful** for developers and browsers

---

## Exercise : Apply Semantic HTML

1. Review your current `index.html`.
2. Replace generic `<div>` and `<span>` tags with semantic tags like `<header>`, `<main>`, `<article>`, `<footer>`, etc.
3. Use `<section>` to group related content with headings.
4. Wrap any side info or links in `<aside>`.
5. Add `<time>` for any date-related content.

---

Great job! You’ve now learned how to write modern, semantic, and meaningful HTML.
