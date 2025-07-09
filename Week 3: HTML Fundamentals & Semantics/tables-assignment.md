#  HTML Tables Assignment (No CSS)

## Objective

Create a full-page **Travel Packages Table** using only **HTML tables** and table attributes—**no CSS** allowed. This assignment is meant to deepen your understanding of complex table structures, `colspan`, `rowspan`, semantic HTML, and nested tables.

---

##  Instructions

You are to build a table for a fictional travel agency titled:

> **Global Escape Travel Packages – 2025**

Use only HTML and built-in table attributes. **No CSS, no JavaScript.**

---

## ✅ Requirements

### 1. Semantic Table Structure

Use all appropriate table tags:
- `<table>`
- `<caption>`
- `<thead>`
- `<tbody>`
- `<tfoot>`
- `<th>` and `<td>`

### 2. Column and Row Spanning

- Use `colspan` for grouping headers.
- Use `rowspan` to merge package rows that share the same destination.

### 3. Table Caption

The table must include a `<caption>` tag with the text:

> `Global Escape Travel Packages – 2025`

### 4. Nested Tables

Simulate a layout by including a **nested table** within the "Optional Services" column to show multiple services per package.

### 5. Footer Row

Add a `<tfoot>` section with a disclaimer like:

> `*Prices are per person in USD and subject to change.`

### 6. Required Columns

Your table must include the following columns:

| Column Name        | Details                                               |
|--------------------|--------------------------------------------------------|
| Destination        | The city or country being offered                      |
| Package Tier       | Basic / Premium / Luxury                               |
| Duration           | Number of days                                         |
| Price              | Use `&dollar;` for dollar sign                         |
| Meals Included     | Use "Yes" or "No"                                      |
| Availability       | List of available months                               |
| Optional Services  | Use a **nested table** to list service options         |

---

##  Sample Table Structure (Preview)

| Destination | Package Tier | Duration | Price | Meals | Availability | Optional Services             |
|-------------|---------------|----------|--------|--------|---------------|-------------------------------|
| Paris       | Basic         | 5        | $1000  | Yes    | April         | Hotel Upgrade, Tour Bus       |
|             | Premium       | 7        | $1800  | Yes    | May           | Airport Pickup, Cruise        |
| Tokyo       | Basic         | 6        | $1200  | No     | June          | Translator, Rail Pass         |
|             | Luxury        | 10       | $3500  | Yes    | April, May     | Spa, Private Guide            |

Use `rowspan` on "Destination" cells where appropriate.


## Submission

- Save your file as: `travel-packages.html`
- Open it in your browser to check formatting.
- Validate your code: [https://validator.w3.org/](https://validator.w3.org/)
- Optional: Submit screenshots of the rendered table for review.


