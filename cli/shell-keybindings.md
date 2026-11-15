# Shell Keybindings

BASH uses same keybindings EMACS since their both GNU programs.

## Reference

- [Essential Keybindings For Bash, Fish and Zsh - DistroTube](https://www.youtube.com/watch?v=XY5qCQcrHns)

## Table of Contents

- [Navigation](#navigation)
- [Edit](#edit)
- [History](#history)
- [Job Control](#job-control)

---

## Navigation

| Key        | Action                      |
| ---------- | --------------------------- |
| `ctrl + a` | move to beginning of line   |
| `ctrl + e` | move to end of line         |
| `ctrl + b` | move backward one character |
| `ctrl + f` | move forward one character  |
| `alt + b`  | move backward one word      |
| `alt + f`  | move forward one word       |

---

## Edit

| Key        | Action                                 |
| ---------- | -------------------------------------- |
| `ctrl + k` | cut from cursor to end of line         |
| `ctrl + u` | cut from cursor to beginning of line   |
| `ctrl + y` | paste most recently cut text at cursor |
| `ctrl + w` | delete word backward                   |
| `alt + d`  | delete word forward                    |

> [!NOTE]
> Cut text is stored in Readline's kill ring, not the system clipboard.

---

## History

| Key        | Action                           |
| ---------- | -------------------------------- |
| `ctrl + p` | previous command (like up arrow) |
| `ctrl + n` | next command (like down arrow)   |
| `!!`       | expand to previous command       |

> [!TIP]
> `sudo !!` expanads to something like `sudo nvim /etc`.

---

## Job Control

| Key        | Action                                                 |
| ---------- | ------------------------------------------------------ |
| `ctrl + z` | suspend the foreground job (if it supports suspension) |
| `fg`       | bring the current job to the foreground                |
| `jobs`     | list current shell's jobs                              |
