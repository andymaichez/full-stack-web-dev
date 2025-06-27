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
