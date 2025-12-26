
## ripgrep (`rg`)

**ripgrep**, often called **`rg`**, is a **fast command-line search tool** for text inside files.

Think of it as **grep on steroids**—it searches **recursively**, is **super fast**, and respects `.gitignore` by default.

---

### Why Developers Use ripgrep

* Quickly **search through codebases** for strings or patterns
* Faster than `grep`, especially for **large projects**
* Respects `.gitignore`, so you don’t get spam from ignored files
* Integrates nicely with **fzf** or other terminal tools for workflow

---

### Basic Usage

```bash
rg "search_term"
```

* Searches for `"search_term"` in **current directory and subdirectories**
* Example: Find all occurrences of `TODO` in a project:

```bash
rg TODO
```

---

### Common Options

| Option    | Description                | Example             |
| --------- | -------------------------- | ------------------- |
| `-i`      | Ignore case                | `rg -i todo`        |
| `-v`      | Invert match               | `rg -v debug`       |
| `-w`      | Match whole words          | `rg -w function`    |
| `-n`      | Show line numbers          | `rg -n TODO`        |
| `--files` | List all files (like `fd`) | `rg --files`        |
| `-g`      | Include/exclude patterns   | `rg -g '*.py' TODO` |

---

### Examples

1. **Search for `main` in Python files only**:

```bash
rg -g "*.py" main
```

2. **Search ignoring case**:

```bash
rg -i "function"
```

3. **Show line numbers for matches**:

```bash
rg -n "TODO"
```

4. **Combine with fzf for interactive search**:

```bash
rg --files | fzf
```

* Search through all project files interactively.

---

### Advanced Use

* **Preview matches with `bat`**:

```bash
rg TODO | fzf --preview 'bat --style=numbers --color=always {}'
```

* Use in **scripts** to automatically find and replace text.
* Integrates with **Neovim/LazyVim** for fast in-editor search.
