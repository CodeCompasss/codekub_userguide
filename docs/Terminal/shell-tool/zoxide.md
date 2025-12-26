

## zoxide

**zoxide** is a **smarter, faster directory jumper** for the terminal.

Think of it as an **improved `cd` command** that learns the directories you use most and lets you jump to them instantly.

---

### Why Developers Use zoxide

* Save time typing long paths
* Quickly navigate **deeply nested directories**
* Learns your **frequently used directories automatically**
* Works with **fuzzy matching** for partial names
* Integrates seamlessly with **bash, zsh, and fish**

---

### Basic Usage

```bash
z <pattern>
```

* Jump to a directory matching `<pattern>`
* Example: If you often go to `/home/user/projects/codekub`, you can type:

```bash
z codekub
```

…and zoxide will take you there instantly.

---

### How It Works

* **Tracks directories** you visit using `cd`
* Stores them in a **database**
* Uses a **ranking system** to prioritize frequently or recently used paths
* Supports **fuzzy search**, so you don’t need exact names

---

### Common Commands

| Command            | Description                              | Example                 |
| ------------------ | ---------------------------------------- | ----------------------- |
| `z <pattern>`      | Jump to matching directory               | `z docs`                |
| `zi <pattern>`     | Jump interactively (select from matches) | `zi proj`               |
| `z -l <pattern>`   | List matching directories                | `z -l proj`             |
| `zoxide query`     | Show stored directories                  | `zoxide query`          |
| `zoxide add <dir>` | Manually add a directory                 | `zoxide add ~/projects` |

---

### Advanced Usage

* Combine with **fzf** for interactive directory selection:

```bash
zoxide query | fzf
```

* Integrate into **scripts** for automation
* Works with **aliases** for super-fast navigation:

```bash
alias p="z projects"
```

* Compatible with **terminal multiplexer** setups (tmux, Zellij)

