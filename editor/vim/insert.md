# Insert

Keybinds in insert mode. Which resembles Emacs keybindings.

## Reference

- [Stop leaving Insert mode - Vimothee](https://www.youtube.com/watch?v=srthFK9hr_M)
- [cli/shell-keybindings.md](/cli/shell-keybindings.md)

---

## Navigation

| Key           | Action         |
| ------------- | -------------- |
| `ctrl + g, j` | Move line up   |
| `ctrl + g, k` | Move line down |

---

## Insertion

| Key        | Action                               |
| ---------- | ------------------------------------ |
| `ctrl + i` | Insert tab                           |
| `ctrl + e` | Character from line below the cursor |
| `ctrl + y` | Character from line above the cursor |
| `ctrl + m` | New line above current position      |
| `ctrl + a` | Last inserted text                   |
| `ctrl + v` | Next key literally                   |

- `ctrl + v, BackSpace` inserts literal `<BS>`.

---

## Deletion

| Key        | Action                       |
| ---------- | ---------------------------- |
| `ctrl + w` | Delete backward by word      |
| `ctrl + h` | Delete backward by character |

---

## Indentation

| Key        | Action  |
| ---------- | ------- |
| `ctrl + t` | Indent  |
| `ctrl + d` | Outdent |

- Where ever your cursor position is on the line.

---

## Register

| Key        | Action               |
| ---------- | -------------------- |
| `ctrl + r` | Insert from register |

- `ctrl + r, %`: Inserts current file's name.
- `ctrl + r, 1`: Inserts from register **1**.

List register:

```vim
:reg<CR>

# alias
:dis<CR>
```

---

## Mode Switching

| Key        | Action                                        |
| ---------- | --------------------------------------------- |
| `ctrl + o` | Execute one command and return to insert mode |

- `ctrl + o, f)`: move cursor to next `)` and switch back to insert.

---

## Completion

| Key                  | Action                     |
| -------------------- | -------------------------- |
| `ctrl + n`           | select next completion     |
| `ctrl + p`           | select previous completion |
| `ctrl + x, ctrl + f` | file completion            |

- `ctrl + n`: selects next without opening completion menu. (if available)
