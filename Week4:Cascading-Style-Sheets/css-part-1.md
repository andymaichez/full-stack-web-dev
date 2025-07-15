Excellent\! With a solid grasp of HTML as the structure of your web pages, it's time to bring them to life with CSS: Cascading Style Sheets. This is where your webpages go from being plain text documents to visually engaging experiences.

-----
# Dive into CSS (Cascading Style Sheets)

CSS is a stylesheet language used to describe the presentation of a document written in HTML. It controls the layout, colors, fonts, spacing, and overall appearance of your web pages. Think of it as the skin, paint, and interior design for your HTML skeleton.

### What is CSS?

  * **Cascading:** Refers to how styles "cascade" down from a general to a more specific level. We'll explore this in detail later.
  * **Style:** Defines how elements should look (color, font, size, position, etc.).
  * **Sheets:** Styles are often stored in separate files (stylesheets) for better organization.

### Why use CSS?

  * **Separation of Concerns:** Keeps content (HTML) separate from presentation (CSS), making your code cleaner, easier to manage, and more maintainable.
  * **Efficiency:** You can define a style once and apply it to multiple HTML elements or even multiple pages, saving time and effort.
  * **Consistency:** Ensures a consistent look and feel across your entire website.
  * **Responsiveness:** Allows you to adapt your website's design for different screen sizes and devices (mobile, tablet, desktop).
  * **Accessibility:** Can improve the readability and user experience for everyone.

-----

## 1\. Ways to Include CSS

There are three primary ways to include CSS in your HTML documents, each with its own use cases and implications.

### 1.1. Inline Styles

  * **How it works:** CSS rules are applied directly to individual HTML elements using the `style` attribute.
  * **Syntax:** `<tagname style="property: value; property2: value2;">Content</tagname>`
  * **Use Case:** Quick, specific styling for a single element. Generally discouraged for larger projects due to poor maintainability and separation of concerns.

**Example:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inline CSS Example</title>
</head>
<body>
    <h1 style="color: blue; font-size: 36px;">This heading is blue and large.</h1>
    <p style="background-color: yellow; padding: 10px;">This paragraph has a yellow background.</p>
</body>
</html>
```

### 1.2. Internal (Embedded) Styles

  * **How it works:** CSS rules are placed within a `<style>` tag in the `<head>` section of an HTML document.

  * **Syntax:**

    ```html
    <head>
        <style>
            /* CSS rules go here */
            body {
                font-family: Arial, sans-serif;
            }
            h1 {
                color: purple;
            }
        </style>
    </head>
    ```

  * **Use Case:** When a single HTML page has unique styles that won't be reused on other pages. Still not ideal for larger sites but better than inline for per-page styling.

**Example:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Internal CSS Example</title>
    <style>
        body {
            font-family: Verdana, sans-serif;
            background-color: #f0f0f0;
        }
        h1 {
            color: maroon;
            text-align: center;
        }
        p {
            line-height: 1.6;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Welcome to My Styled Page</h1>
    <p>This paragraph and heading are styled using internal CSS defined in the head section.</p>
    <p>All paragraphs on this page will inherit these styles.</p>
</body>
</html>
```

### 1.3. External Styles (Recommended\!)

  * **How it works:** CSS rules are stored in a separate `.css` file and linked to the HTML document using the `<link>` tag in the `<head>` section.
  * **Syntax (in HTML file):** `<link rel="stylesheet" href="path/to/your/styles.css">`
      * `rel="stylesheet"`: Specifies the relationship between the HTML and the linked file.
      * `href`: Specifies the path to the CSS file.
  * **Use Case:** The most common and recommended method for almost all web development. It promotes separation of concerns, reusability, and efficient caching by browsers.

**Example:**

`index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>External CSS Example</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Our Company Blog</h1>
    </header>
    <main>
        <p>This content is styled by our external stylesheet.</p>
        <button>Learn More</button>
    </main>
</body>
</html>
```

`styles.css` (in the same folder as `index.html`):

```css
/* styles.css */
body {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #e8f5e9; /* Light green background */
}

header {
    background-color: #4CAF50; /* Green header */
    color: white;
    padding: 15px;
    text-align: center;
}

h1 {
    font-size: 2.5em;
    margin-bottom: 10px;
}

p {
    font-size: 1.1em;
    color: #333;
    line-height: 1.8;
}

button {
    background-color: #008CBA; /* Blue button */
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
}

button:hover {
    background-color: #005f7a;
}
```

### Exercise 1.1: Experiment with CSS Inclusion Methods

1.  Open your `index.html` from the HTML course.
2.  **Inline:** Add a `style` attribute to your main `<h1>` and change its color to `red` and `text-align` to `center`.
3.  **Internal:** In the `<head>` section of `index.html`, add a `<style>` tag. Inside it, set the `background-color` of the `body` to a light grey (`#f0f0f0`). Also, set all `p` elements to `font-family: Georgia, serif;`.
4.  **External:** Create a new file named `my-styles.css` in the same folder.
      * In `my-styles.css`, add a rule: `h2 { color: green; border-bottom: 2px solid green; }`.
      * Link this `my-styles.css` file to your `index.html` using a `<link>` tag in the `<head>`.
5.  Save both files and open `index.html` in your browser. Observe how the styles are applied. Notice which styles might override others (hint: inline usually wins).

-----

## 2\. CSS Selectors

Selectors are patterns used to select the HTML elements you want to style. Without selectors, CSS wouldn't know which parts of your document to apply rules to.

### 2.1. Element (Type) Selector

Selects all instances of a specific HTML element.

  * **Syntax:** `elementname { property: value; }`

  * **Example:**

    ```css
    p {
        font-size: 16px;
        color: #444;
    }
    h1 {
        text-transform: uppercase;
    }
    ```

    This will apply the styles to all `<p>` tags and all `<h1>` tags on the page.

### 2.2. Class Selector

Selects all elements that have a specific `class` attribute.

  * **Syntax:** `.classname { property: value; }`

  * Multiple elements can share the same class. An element can also have multiple classes (e.g., `<p class="intro highlight">`).

  * **Example:**

    HTML:

    ```html
    <p class="highlight">This text will be highlighted.</p>
    <span class="highlight">And this span too.</span>
    <h2 class="section-title">Section Heading</h2>
    ```

    CSS:

    ```css
    .highlight {
        background-color: yellow;
        font-weight: bold;
    }
    .section-title {
        color: darkred;
        font-family: 'Open Sans', sans-serif;
    }
    ```

### 2.3. ID Selector

Selects a unique element that has a specific `id` attribute.

  * **Syntax:** `#idname { property: value; }`

  * **Important:** An `id` must be unique within a single HTML document. Use IDs sparingly, primarily for JavaScript manipulation or specific page sections, as classes are more flexible for styling.

  * **Example:**

    HTML:

    ```html
    <div id="main-content">
        <p>This is the main content area.</p>
    </div>
    <footer id="page-footer">
        <p>&copy; 2025</p>
    </footer>
    ```

    CSS:

    ```css
    #main-content {
        border: 1px solid #ccc;
        padding: 20px;
        margin-top: 20px;
    }
    #page-footer {
        text-align: center;
        font-size: 0.9em;
        color: #666;
    }
    ```

### 2.4. Universal Selector

Selects all HTML elements on the page.

  * **Syntax:** `* { property: value; }`

  * **Use Case:** Often used for global resets (e.g., removing default margins/padding).

  * **Example:**

    ```css
    * {
        box-sizing: border-box; /* A very common reset property */
        margin: 0;
        padding: 0;
    }
    ```

### 2.5. Grouping Selectors

Apply the same styles to multiple selectors by separating them with commas.

  * **Syntax:** `selector1, selector2, selector3 { property: value; }`

  * **Example:**

    ```css
    h1, h2, h3 {
        font-family: 'Roboto Condensed', sans-serif;
        color: #2c3e50;
        margin-bottom: 15px;
    }
    p, li {
        line-height: 1.6;
    }
    ```

### Exercise 2.1: Practicing Selectors

1.  Open your `my-styles.css` file.
2.  Add a class named `warning` to one of your paragraphs in `index.html`. In `my-styles.css`, create a rule for `.warning` that sets `color: red;` and `font-weight: bold;`.
3.  Add an `id` named `special-heading` to your `<h2>` tag in `index.html`. In `my-styles.css`, create a rule for `#special-heading` that sets `background-color: lightblue;` and `padding: 10px;`.
4.  Using a grouping selector, set the `border-radius` to `5px` for all `button` and `input[type="submit"]` elements. (You might need to add a simple button to your HTML if you don't have one).
5.  Add the universal selector `*` rule `box-sizing: border-box;` at the very top of your `my-styles.css`.
6.  Save both files and observe the changes in your browser.

-----

## 3\. The Cascade, Specificity, and Inheritance

These are fundamental concepts in CSS that determine which styles get applied when multiple rules conflict.

### 3.1. The Cascade

The "C" in CSS stands for **Cascading**. It defines the order in which CSS rules are applied and which rules take precedence when there are conflicting declarations. Rules "cascade" down through different levels:

  * **Browser default styles:** Every browser has its own default stylesheet (e.g., headings are bold, links are blue and underlined).
  * **User styles:** Users can set their own stylesheets (e.g., for accessibility reasons).
  * **Author styles:** The styles defined by you (inline, internal, external).
  * **Order of Inclusion:** If you link multiple external stylesheets, the last one linked takes precedence for conflicting rules.
  * **Rule Order:** Within a single stylesheet, the last rule declared for the same selector and property wins.
  * `!important`: This declaration overrides all other rules, but its use is highly discouraged as it makes debugging and maintaining CSS very difficult. Only use it as a last resort in very specific situations.

**Example of Rule Order:**

```css
/* styles.css */
p {
    color: blue;
}
/* Later in the same file */
p {
    color: green; /* This will win */
}
```

### 3.2. Specificity

**Specificity** is a scoring system that determines which CSS rule gets applied to an element when multiple rules target the same element and property. A more specific rule always wins over a less specific one.

**Specificity Hierarchy** (from least to most specific):

  * **Universal selector (`*`):** 0,0,0,0 (zero specificity)
  * **Element selectors (`p`, `h1`, `div`):** 0,0,0,1 for each element.
  * **Class selectors (`.my-class`):** 0,0,1,0 for each class.
  * **Attribute selectors (`[type="text"]`) and Pseudo-classes (`:hover`, `:first-child`):** 0,0,1,0
  * **ID selectors (`#my-id`):** 0,1,0,0 for each ID.
  * **Inline styles (`style=""`):** 1,0,0,0 (highest specificity, overrides everything except `!important`)

**Calculating Specificity:**

You can think of specificity as a four-digit number (`a, b, c, d`):

  * `a`: 1 if inline style, 0 otherwise.
  * `b`: Number of ID selectors.
  * `c`: Number of class selectors, attribute selectors, and pseudo-classes.
  * `d`: Number of element selectors and pseudo-elements (`::before`, `::after`).

**Example:**

```css
/* Rule 1: Specificity (0,0,0,1) */
p { color: red; }

/* Rule 2: Specificity (0,0,1,0) */
.text-style { color: blue; }

/* Rule 3: Specificity (0,1,0,0) */
#main-paragraph { color: green; }
```

HTML: `<p class="text-style" id="main-paragraph">Hello World</p>`

In this case, `#main-paragraph` (green) will win because it has the highest specificity score (0,1,0,0).

**Important Note:** If two rules have the exact same specificity, the one declared last in the stylesheet wins (this is where the "cascade" order comes into play).

### 3.3. Inheritance

Some CSS properties are **inherited** by child elements from their parent elements. This means you don't have to apply the same style to every element individually.

**Commonly Inherited Properties:**

  * `color`
  * `font-family`
  * `font-size`
  * `font-weight`
  * `line-height`
  * `text-align`
  * `list-style`

**Non-Inherited Properties** (most box model properties, etc.):

  * `margin`
  * `padding`
  * `border`
  * `background-color`
  * `width`, `height`

**Example of Inheritance:**

```css
/* styles.css */
body {
    font-family: Arial, sans-serif;
    color: #333;
}
/* index.html */
<body>
    <p>This text will be Arial and #333 because it inherits from body.</p>
    <div>
        <span>This span also inherits Arial and #333.</span>
    </div>
</body>
```

### Exercise 3.1: Understanding Cascade, Specificity, and Inheritance

In your `index.html`, ensure you have an external `my-styles.css` linked.

**Specificity Test:**

In `my-styles.css`:

```css
p { color: red; }
.intro-paragraph { color: blue; } /* Add this class to a <p> in HTML */
#my-unique-para { color: green; } /* Add this ID to the *same* <p> in HTML */
```

In `index.html`, add this paragraph: `<p class="intro-paragraph" id="my-unique-para" style="color: purple;">Which color will I be?</p>`

Observe the color. Then, remove the `style` attribute and re-check.

**Cascade Order Test:**

In `my-styles.css`, add:

```css
h1 { font-size: 30px; }
/* Add this rule *below* the previous h1 rule */
h1 { font-size: 40px; }
```

Observe your `<h1>`. Then, swap the order of the two `h1` rules.

**Inheritance Test:**

In `my-styles.css`, set `body { font-size: 18px; line-height: 1.5; }`.

Observe your paragraphs and other text. They should inherit these styles.

Now, explicitly set `p { font-size: 14px; }`. Notice how the paragraph overrides the inherited `font-size` but still inherits `line-height`.

Experiment with these to truly grasp how CSS decides which rules to apply.

-----

## 4\. Common CSS Properties

Let's explore some of the most frequently used CSS properties to style your web pages.

### 4.1. Text Styling

  * **`color`:** Sets the text color.

      * **Values:** Named colors (`red`), Hex codes (`#RRGGBB`), RGB (`rgb(r,g,b)`), RGBA (`rgba(r,g,b,a)` where 'a' is alpha for transparency), HSL (`hsl(h,s,l)`).

      * **CSS**

        ```css
        p { color: blue; }
        h1 { color: #336699; }
        span { color: rgb(255, 0, 0); }
        ```

  * **`font-family`:** Specifies the font for an element. Provide a comma-separated list of preferred fonts (fallback fonts).

      * **CSS**

        ```css
        body { font-family: Arial, sans-serif; }
        h1 { font-family: 'Times New Roman', serif; }
        ```

      * **Note:** If you want to use custom fonts, you'll need to link them (e.g., from Google Fonts) in your HTML's `<head>` using a `<link>` tag.

  * **`font-size`:** Sets the size of the font.

      * **Values:** `px` (pixels), `em` (relative to parent's font size), `rem` (relative to root HTML's font size), `%` (percentage).

      * **CSS**

        ```css
        p { font-size: 16px; }
        h2 { font-size: 1.5em; /* 1.5 times the parent's font size */ }
        body { font-size: 100%; } /* Default browser font size */
        ```

  * **`font-weight`:** Sets the thickness of the characters.

      * **Values:** `normal`, `bold`, `bolder`, `lighter`, or numeric values `100` to `900` (e.g., `400` is normal, `700` is bold).

      * **CSS**

        ```css
        strong { font-weight: bold; }
        .thin-text { font-weight: 300; }
        ```

  * **`font-style`:** Sets text to italic or normal.

      * **Values:** `normal`, `italic`, `oblique`.

      * **CSS**

        ```css
        em { font-style: italic; }
        ```

  * **`text-align`:** Aligns the text within its containing element.

      * **Values:** `left`, `right`, `center`, `justify`.

      * **CSS**

        ```css
        h1 { text-align: center; }
        p { text-align: justify; }
        ```

  * **`text-decoration`:** Adds or removes decorations from text.

      * **Values:** `none`, `underline`, `overline`, `line-through`.

      * **CSS**

        ```css
        a { text-decoration: none; /* Removes default underline from links */ }
        .crossed-out { text-decoration: line-through; }
        ```

  * **`line-height`:** Sets the height of each line of text. Often used to improve readability.

      * **Values:** A number (multiplies font size), a length (px, em), a percentage.

      * **CSS**

        ```css
        p { line-height: 1.6; /* 1.6 times the font-size */ }
        ```

  * **`letter-spacing`:** Sets the space between characters.

      * **CSS**

        ```css
        h1 { letter-spacing: 2px; }
        ```

  * **`text-transform`:** Controls the capitalization of text.

      * **Values:** `none`, `uppercase`, `lowercase`, `capitalize`.

      * **CSS**

        ```css
        h2 { text-transform: uppercase; }
        ```

### 4.2. Colors & Backgrounds

  * **`background-color`:** Sets the background color of an element.

      * **Values:** Same as `color` (named, hex, rgb, rgba, hsl).

      * **CSS**

        ```css
        body { background-color: #f8f8f8; }
        .card { background-color: white; }
        ```

  * **`background-image`:** Sets an image as the background.

      * **Values:** `url('path/to/image.jpg')`.

      * **CSS**

        ```css
        body { background-image: url('images/bg.png'); }
        ```

  * **`background-repeat`:** How a background image should repeat.

      * **Values:** `repeat` (default), `no-repeat`, `repeat-x` (horizontally), `repeat-y` (vertically).

      * **CSS**

        ```css
        body { background-repeat: no-repeat; }
        ```

  * **`background-position`:** Sets the starting position of a background image.

      * **Values:** `top`, `bottom`, `left`, `right`, `center`, or `x% y%`, or `xpx ypx`.

      * **CSS**

        ```css
        body { background-position: center top; }
        ```

  * **`background-size`:** Specifies the size of the background image.

      * **Values:** `auto`, `cover` (scales to cover the entire element), `contain` (scales to fit within the element without cropping), or `length` (`px`, `%`).

      * **CSS**

        ```css
        body { background-size: cover; }
        ```

  * **`background` (Shorthand):** A shorthand property to set multiple background properties in one declaration. Order matters.

      * **CSS**

        ```css
        body {
            background: #f8f8f8 url('images/bg.png') no-repeat center top / cover;
            /* color image repeat position / size */
        }
        ```

### 4.3. The Box Model

Every HTML element is treated as a rectangular box by the browser. The CSS **Box Model** describes how these boxes are rendered and how space is distributed around elements.

```
+-----------------------------------+
|             Margin                |
|  +-----------------------------+  |
|  |           Border            |  |
|  |  +-----------------------+  |  |
|  |  |       Padding         |  |  |
|  |  |  +-----------------+  |  |  |
|  |  |  |     Content     |  |  |  |
|  |  |  +-----------------+  |  |  |
|  |  +-----------------------+  |  |
|  +-----------------------------+  |
+-----------------------------------+
```

  * **Content:** The actual content of the element (text, image, video, etc.).

  * **Padding:** Space between the content and the border. It's the element's inner spacing.

  * **Border:** A line that goes around the padding and content.

  * **Margin:** Space outside the border, pushing other elements away. It's the element's outer spacing.

  * **`width` and `height`:** Set the dimensions of the content area.

      * **CSS**

        ```css
        img { width: 300px; height: auto; /* auto maintains aspect ratio */ }
        div { width: 50%; height: 200px; }
        ```

  * **`box-sizing`:** A crucial property for controlling how `width` and `height` are calculated.

      * `content-box` (default): `width`/`height` only apply to the content area. Padding and border are added to the total `width`/`height`.

      * `border-box`: `width`/`height` include content, padding, and border. This makes layout much more predictable. It's a best practice to set `box-sizing: border-box;` globally using the universal selector.

      * **CSS**

        ```css
        * {
            box-sizing: border-box; /* Highly recommended! */
        }
        ```

  * **`padding`:** Sets the padding area.

      * Can be set for all sides or individually:

          * `padding: 20px;` (all 4 sides)
          * `padding: 10px 20px;` (top/bottom, left/right)
          * `padding: 10px 20px 30px;` (top, left/right, bottom)
          * `padding: 10px 20px 30px 40px;` (top, right, bottom, left - clockwise)

      * `padding-top`, `padding-right`, `padding-bottom`, `padding-left`

      * **CSS**

        ```css
        .card { padding: 15px; }
        button { padding: 10px 20px; }
        ```

  * **`margin`:** Sets the margin area.

      * Shorthand and individual properties work the same as padding.

      * **Margin Collapse:** Vertical margins between adjacent elements or parent/child elements can "collapse" into a single margin. Horizontal margins never collapse.

      * `margin: 0 auto;`: A common trick to horizontally center a block-level element that has a defined width.

      * **CSS**

        ```css
        h1 { margin-bottom: 20px; }
        img { margin: 10px; }
        .container { width: 800px; margin: 0 auto; }
        ```

  * **`border`:** Sets the border around an element.

      * **Shorthand:** `border: width style color;`

      * **Individual properties:** `border-width`, `border-style`, `border-color`.

      * **Common styles:** `solid`, `dotted`, `dashed`, `double`.

      * **`border-radius`:** Rounds the corners of the border.

      * **CSS**

        ```css
        p { border: 1px solid #ccc; }
        div { border-left: 5px solid blue; }
        button { border-radius: 5px; }
        img { border-radius: 50%; /* Makes a circular image */ }
        ```

### Exercise 4.1: Styling with Properties

Open your `index.html` and `my-styles.css` files.

**Global Styles:**

1.  Set `body` to have a `font-family` of your choice (e.g., `Lato, sans-serif`), a `line-height` of `1.6`, and a `background-color` of a very light shade (e.g., `#f8f8f8`).
2.  Add `* { box-sizing: border-box; margin: 0; padding: 0; }` at the top of your `my-styles.css`.

**Headings:**

1.  Style all `h1` elements: `color`, `text-align: center;`, `margin-bottom`.
2.  Style all `h2` elements: `color`, `text-transform: uppercase;`, `border-bottom: 1px solid;`, `padding-bottom`.

**Paragraphs:**

1.  Give all `p` elements some `padding` (e.g., `10px`).
2.  Add a subtle `border` (e.g., `1px dashed #eee`) to paragraphs.

**Links:**

1.  Remove the default `text-decoration` from all `a` tags.
2.  Change the `color` of links to something other than blue.

**Images:**

1.  Set a `width` (e.g., `300px`) and `height: auto;` for all `img` tags.
2.  Add a `border` to images (e.g., `3px solid #ddd`).
3.  Add `margin: 15px;` to space them out.
4.  Give images a `border-radius: 8px;` for slightly rounded corners.

**Buttons/Inputs (if you have them):**

1.  Give your submit button or any `<button>` a `background-color`, `color`, `padding`, `border: none;`, and `border-radius`.
2.  Add a `:hover` effect.

Save and view your page. Notice the significant visual improvements\!

-----

## Mini-Project: Enhance Your Portfolio Page

Let's take the "Personal Portfolio Page" HTML you created and give it some style\!

**Goal:** Apply CSS to make your portfolio page visually appealing and structured.

**Requirements:**

  * **External CSS:** Create a new `style.css` file in your portfolio folder and link it to your `index.html`. All CSS should be in this external file.
  * **Global Styles:**
      * Set `box-sizing: border-box;` globally.
      * Apply a readable `font-family` (e.g., `Arial, sans-serif`) to the `body`.
      * Choose a light `background-color` for the `body`.
      * Set a default `line-height` for `p` elements.
  * **Header Styling:**
      * Give your `<header>` a distinct `background-color`, `color` for text, `padding`, and `text-align: center;`.
      * Style your `<h1>` inside the header (e.g., `font-size`, `margin-bottom`).
  * **Navigation Styling:**
      * Style your `<nav>` (e.g., `display: block; text-align: center;`).
      * Remove bullet points from the `<ul>` within `nav` (`list-style: none;`).
      * Remove default underlines from `<a>` tags within `nav` and set their `color`.
      * Add `padding` to `<a>` tags and make them `display: inline-block;` for spacing.
      * Add a `:hover` pseudo-class effect to your nav links (e.g., change `background-color` or `color` on hover).
  * **Section Styling:**
      * Give each `<section>` a `padding` and a `margin-bottom`.
      * Add a light `border` or `background-color` to differentiate sections if desired.
      * Center your section `<h2>` headings.
  * **Image Styling:**
      * Style your `<img>` in the "About Me" section: give it a `width` (e.g., `200px`), `height: auto;`, `border-radius: 50%;` (for a circle), and `display: block; margin: 0 auto;` to center it.
  * **List Styling (Skills):**
      * Adjust `margin-left` and `padding-left` for the `<ul>` to control indentation.
      * Change the `list-style-type` (e.g., `square`, `circle`).
  * **Form Styling (Contact):**
      * Style your form `input` fields and `textarea`: give them `width: 100%;`, `padding`, `margin-bottom`, `border`, and `border-radius`.
      * Style your submit button: `background-color`, `color`, `padding`, `border: none;`, `cursor: pointer;`. Add a `:hover` effect.
  * **Footer Styling:**
      * Give your `<footer>` a `background-color`, `color`, `padding`, and `text-align: center;`.

**Steps:**

1.  Open your `portfolio/index.html` file.
2.  Create `portfolio/style.css`.
3.  Link `style.css` in `index.html`.
4.  Start adding CSS rules to `style.css` based on the requirements.
5.  Continuously save and check your page in the browser to see the live updates.

You've now taken a significant leap from just structuring content to actively designing its appearance. CSS is a vast and powerful language, but mastering these fundamental concepts of inclusion, selectors, cascade, specificity, inheritance, and common properties will provide an excellent foundation for building beautiful and functional web pages.
