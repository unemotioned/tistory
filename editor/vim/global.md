# Global

```vim
:g/<pattern>/<cmd>
```

## Print

`p` at cmd, or nothing, will print by default.

---

## Delete

Delete every line with a matching pattern:

```vim
:g/vscode/d

" case insensitive with "i" option
:g/vscode/id
```

---

## Normal

You can use the `normal` command with `global`:

```vim
:g/neovim/norm A is awesome
```

- Add `A is Awesome` at the end of lines that contain `neovim`.

---

## Reverse

Delete every line that does not contain the string `vim`:

```vim
:v/vim/d
```
