
# Terminal Project – Linux Commands Practice

You’ve been assigned to build a terminal project using **Linux commands only**. The goal is to strengthen your understanding of Linux terminal usage, file system navigation, and Git version control.

---

## Project Instructions

1. **Create a GitHub repository** named: `Terminal_Commands`.
2. **Clone** the repository locally on your machine:
   ```bash
   git clone https://github.com/<your-username>/Terminal_Commands.git
   ```
3. Inside the `Terminal_Commands` folder:
   - Create three main directories:
     - `html/`
     - `css/`
     - `js/`
   - Inside each directory, create the following subfolders:
     - `snippets/` — store code samples
     - `notes/` — store written notes and explanations

4. Create the following files and structure using terminal commands only:

---

## Expected Folder & File Structure

```
Terminal_Commands/
├── README.md
├── hello-world.js            
├── dom.txt                       
├── html/
│   ├── notes/
│   │   ├── index.html
│   │   └── semantic-tags.md      # Copied from snippets
│   └── snippets/
│       ├── semantic.html
│       └── semantic-tags.md
├── css/
│   ├── notes/
│   │   └── style.css
│   └── snippets/
│       └── flexbox.css
├── js/
│   ├── notes/
│   │   ├── script.js
│   │   └── hello-world.js        # Moved from root
│   └── snippets/
│       ├── dom-example.js
│       └── dom-overview.txt      # Renamed from dom.txt and copied here
├── commands_used.txt           
```

---

## Required Terminal Tasks

Perform all the following using **Linux terminal commands only**:

- Use `mkdir`, `touch`, `mv`, `cp`, `echo`, `vi`, etc.
- Create all directories and files as shown above.
- **Add sample content (1–2 lines)** into every file (code or notes). i.e generate some few content for each file.
- Copy `semantic-tags.md` from `html/snippets/` to `html/notes/`.
- Move `hello-world.js` from the **root** to `js/notes/`.
- Rename `dom.txt`  to `dom-overview.txt` inside `js/snippets/`.
- Use `git` to:
  - Track changes
  - Stage and commit files with meaningful commit messages
  - Push to your GitHub repo

---


- Create a `commands_used.txt` file in the project root.
- Record the Linux commands you used for this project with a short description each. Examples are as follows:
  ```bash
  mkdir html        # Create a directory named html
  touch script.js   # Create a new file
  mv hello.js js/   # Move file to another folder
  ```

---

## Submission Checklist

- [ ] Folder and file structure matches expected output.
- [ ] All content created using terminal commands only.
- [ ] Files contain sample content (code or notes).
- [ ] Project is pushed to GitHub under the correct repository name.
- [ ] `commands_used.txt` exists and documents terminal usage.

---
