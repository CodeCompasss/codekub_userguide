

## fzf

**`fzf`** stands for **Fuzzy Finder**.

It is a **command-line interactive search tool** that lets you **find files, directories, or text efficiently** using fuzzy matching.

---

### Why Developers Use `fzf`

* Quickly **search through large directories or command history**
* Navigate **files and Git branches** without typing full names
* Combine with other tools like `fd`, `git`, or `ripgrep` for **powerful workflows**
* Saves time compared to manually scrolling or typing long names

---

### Basic Usage

```bash
fzf
```

* Opens an interactive search menu for standard input.
* Example: List files and select one interactively:

```bash
ls | fzf
```

* Use arrow keys or type a few letters to **filter and select a file**.

---

### File Searching with `fzf`

Combine `fzf` with `fd`:

```bash
fd . | fzf
```

* `fd .` lists all files recursively
* `fzf` lets you **fuzzy search and select**

---

### Git Integration

```bash
git branch | fzf
```

* Select a branch interactively to **checkout**:

```bash
git checkout $(git branch | fzf)
```

---

### Command History Search

```bash
history | fzf
```

* Find a previous command quickly and **reuse it**.

---

### Key Features

* **Fuzzy matching**: you don’t need exact names
* **Interactive interface** with arrow keys and search
* **Customizable keybindings** and actions
* Works with **files, directories, git branches, processes, history**

