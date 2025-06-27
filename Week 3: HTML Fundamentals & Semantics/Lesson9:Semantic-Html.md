
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
