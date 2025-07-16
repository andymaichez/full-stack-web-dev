# Assignment: Build a Personal Portfolio Website with HTML

## Overview

Create a multi-page personal portfolio website using only HTML. This assignment covers all major HTML topics, including structure, tags, attributes, text formatting, lists, links, images, tables, forms, and semantic HTML. By completing this project, you will demonstrate your mastery of HTML fundamentals.

---

## Project Structure

Create the following files and folders:

```
/portfolio-project/
  ├── index.html
  ├── about.html
  ├── gallery.html
  ├── contact.html
  ├── /images/
  │      ├── profile.jpg
  │      ├── portfolio1.png
  │      └── logo.svg
```

---

## Instructions

### 1. General Requirements

- Every HTML file must have a complete structure:  
  `<!DOCTYPE html>`, `<html lang="en">`, `<head>`, and `<body>`.
- Use semantic tags: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<figure>`, `<figcaption>`, `<time>`.
- Organize images in the `/images/` folder.

---

### 2. Page Details

#### **index.html** (Home Page)

- Add a `<header>` with your site title and a navigation bar (`<nav>`) linking to all pages.
- Use `<main>` and `<section>` for your introduction.
- Include a profile image using `<img>`.
- List your hobbies or interests using an unordered list (`<ul>`).
- `<footer>` with copyright and contact details.

#### **about.html**

- Use a semantic layout: `<header>`, `<nav>`, `<main>`.
- Add a biography with headings (`<h1>`, `<h2>`) and paragraphs.
- Create an ordered list (`<ol>`) of achievements or career milestones.
- Add a table (“Skills Overview” or “Experience”) with at least 3 columns and 4 rows, using `<thead>`, `<tbody>`, `<tfoot>`, and at least one `colspan` or `rowspan`.
- Make a description list (`<dl>`) for a FAQ or glossary.
- Use `<time>` to show important dates (e.g., graduation).
- Add an `<aside>` with quick facts or external resource links.

#### **gallery.html**
- Set up the basic HTML document structure (DOCTYPE, `<html>`, `<head>`, `<body>`, etc.)
- Inside the `<body>`, create a `<section>` to hold your images
- Give this section a descriptive heading using an `<h2>` tag
- Use an unordered list (`<ul>`) to create three categories: Travel, Work, and Hobbies
- Each category should be a list item (`<li>`) and contain its own nested list for images i.e inside each `<li> </li>` you should have another nested `<ul> </ul>` which has the image
- In each nested list, add one image using the appropriate image tag
- For each image:

  - Set the source to one of your image files
  - Include alternative text for accessibility
  - Add a caption using a suitable element
- Make one image (for example, under the "Travel" section) clickable so that it opens a link in a new tab. The image source (src) should be an external URL (i.e., an absolute path from a site like Unsplash or another online source), not a file saved in your local images folder.

**Expected Outcome**
``` 
   - Display a collection of at least 3 images (use `<figure>` and `<figcaption>`).
   - Each image must have descriptive `alt` text and `width`/`height` attributes.
   - Make at least one image a clickable link to an external site.
   - Use nested lists to describe categories (e.g., “Travel”, “Work”, “Hobbies”).
```

#### **contact.html**

- Create a contact form using `<form>`, with:
  - Text input for Name (**required**)
  - Email input (**required**)
  - Textarea for Message
  - Radio buttons for preferred contact method (Email, Phone)
  - Checkbox for newsletter subscription
  - Submit and Reset buttons
  - File upload input (e.g., “Attach a resume”)
- Use `<label>` for all form fields.
- Use `placeholder` attributes.
- Add a mailto link and tel link for alternative contact.
- Create an anchor/bookmark link to jump to the form section.
- Include a `<footer>`.

---

### 3. HTML Features to Demonstrate

- Headings (`<h1>`–`<h3>`)
- Paragraphs
- Line breaks (`<br>`) and horizontal rules (`<hr>`)
- Bold and italic text (`<strong>`, `<b>`, `<em>`, `<i>`)
- Marked (`<mark>`) and small text (`<small>`)
- Superscript (`<sup>`) and subscript (`<sub>`)
- Unordered, ordered, and description lists (including nested lists)
- Anchor links (internal, external, mailto, tel, and bookmarks)
- Images (with `alt`, `width`, `height`, and links)
- Tables (with headers, footers, and merged cells)
- Forms (various input types, labels, required fields, placeholders)
- Semantic HTML layout (replace unnecessary `<div>`s and `<span>`s)

---

## Best Practices

- Use semantic tags wherever possible.
- Always provide descriptive `alt` text for images.
- Use `id` and `class` for navigation and organization.
- Quote all attribute values.
- Validate your HTML (e.g., [W3C Validator](https://validator.w3.org/)).
- Test all links and forms for correct behavior.
- Write clear, readable HTML code.

---

## Submission

- Ensure all required pages and features are completed.
- Double-check file and folder organization.
- Push your code to the repository.
- (Optional) Include screenshots of your pages in a `/screenshots/` folder.

---

**Good luck! This assignment will give you a solid foundation in HTML and web page structure.**
