

## exa

**`exa`** is a modern replacement for the `ls` command.

It lists **files and directories** in a terminal, but in a **more readable and visually appealing way**.

---

### Why Developers Use `exa`

* **Colorized output** by file type (folders, executables, etc.)
* Shows **git status** if inside a repository
* Supports **icons and tree views**
* More **user-friendly than `ls`**, especially for beginners

---

### Basic Usage

```bash
exa
```

* Lists files in the current directory.

```bash
exa -l
```

* Long listing format (like `ls -l`), shows permissions, owner, size, and date.

```bash
exa -la
```

* Show **all files**, including hidden ones (`.` files).

---

### Advanced Usage

| Option  | Description          | Example     |
| ------- | -------------------- | ----------- |
| `-T`    | Tree view            | `exa -T`    |
| `--git` | Show Git status      | `exa --git` |
| `-h`    | Human-readable sizes | `exa -lh`   |
| `-S`    | Sort by size         | `exa -lS`   |
| `-r`    | Reverse order        | `exa -lr`   |

💡 Example: **Tree view with Git info**

```bash
exa -T --git
```
