

## fd

**`fd`** is a **modern, fast, and user-friendly alternative to `find`** in Linux.

It is used to **search for files and directories** in your filesystem.

---

### Why Developers Use `fd`

* **Faster than `find`** – uses smart defaults and parallelism
* **Simpler syntax** – easier for beginners to remember
* **Colorized output** – makes results readable
* **Flexible filtering** – supports regex, file types, and exclusions

---

### Basic Usage

```bash
fd <pattern>
```

* Searches for files/folders matching `<pattern>` in the **current directory** and subdirectories.
* Example: Find all `.txt` files:

```bash
fd .txt
```

---

### Common Options

| Option     | Description                        | Example                                        |
| ---------- | ---------------------------------- | ---------------------------------------------- |
| `-t f`     | Search **files only**              | `fd -t f README`                               |
| `-t d`     | Search **directories only**        | `fd -t d src`                                  |
| `-e <ext>` | Match **specific extension**       | `fd -e md` (all Markdown files)                |
| `-x <cmd>` | Execute command on **each result** | `fd -e log -x rm {}` (delete all `.log` files) |
| `-i`       | **Ignore case**                    | `fd -i readme`                                 |

---

### Examples

1. **Search for a file named `config.yaml`** anywhere:

```bash
fd config.yaml
```

2. **Find all `.py` files in a project**:

```bash
fd -e py
```

3. **Search directories named `tests`**:

```bash
fd -t d tests
```

4. **Delete all `.tmp` files safely**:

```bash
fd -e tmp -x rm {}
```

---

### Advanced Usage

* Combine with `grep` to **search inside files**:

```bash
fd -e txt -x grep "TODO" {}
```

* Exclude directories (like `.git` or `node_modules`):

```bash
fd --exclude .git --exclude node_modules
```

* Integrate with scripts for **automation** or **CI/CD pipelines**.
