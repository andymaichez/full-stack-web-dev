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
