

## Remote Access & File Transfer (How Engineers Work Across Machines)

As an engineer, you will often work with **other computers**:

* servers
* cloud machines
* lab systems
* remote Linux boxes

To do this **securely**, engineers use **SSH and related tools**.

---

## What Is SSH?

**SSH (Secure Shell)** is a **secure way to connect to another computer over a network**.

It lets you:

* open a remote terminal
* run commands on another machine
* manage servers securely

Everything is **encrypted**.

---

### Beginner Mental Model

Think of SSH as:

> “A secure remote terminal.”

You type commands on your laptop —
they run on another computer.

---

## OpenSSH (The Most Common SSH Implementation)

**OpenSSH** is the most widely used software that provides SSH.

It comes in two main parts:

* **openssh-client**
* **openssh-server**

---

## openssh-client (Connect to Other Computers)

The **OpenSSH client** is used when **you want to connect to another machine**.

Example:

```bash
ssh user@server_ip
```

Used for:

* logging into remote servers
* accessing cloud machines
* working on college lab systems

Most systems already have this installed.

---

## openssh-server (Allow Others to Connect to You)

The **OpenSSH server** runs on the **machine you want to connect to**.

It allows:

* incoming SSH connections
* secure remote access

Used on:

* servers
* lab machines
* virtual machines

Without `openssh-server`, others cannot SSH into that machine.

---

### Simple Difference

| Tool           | Purpose                            |
| -------------- | ---------------------------------- |
| openssh-client | Connect **to** other machines      |
| openssh-server | Allow others to connect **to you** |

---

## What Is rsync?

**rsync** is a **fast and efficient file transfer tool**.

It copies files:

* locally
* between computers
* over SSH

Only **changes** are transferred, not the entire file.

---

## Why Engineers Use rsync

### ⚡ Efficient Transfers

* Transfers only modified parts
* Saves time and bandwidth

---

### 🔐 Secure

When used with SSH, rsync is:

* encrypted
* safe for remote transfers

---

### 🔁 Reliable for Backups

Engineers use rsync for:

* syncing project folders
* backups
* moving large directories

---

## Beginner Mental Model

Think of rsync as:

> “Smart copy that works locally or remotely.”

---

## Simple rsync Example

Copy a folder to a remote server:

```bash
rsync -av project/ user@server:/home/user/project/
```

Only changes are sent.

---

## How Engineers Use These Together

Typical workflow:

1. Use **SSH** to log into a server
2. Use **rsync** to upload or download files
3. Work remotely as if the machine is local

This is a core Linux skill.
