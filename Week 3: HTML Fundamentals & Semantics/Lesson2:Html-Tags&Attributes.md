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

