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
