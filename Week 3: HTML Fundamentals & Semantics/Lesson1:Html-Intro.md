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
    //content goes here
    // all the content you want visible
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

