# Shell Keybindings

`Bash` keybindings on Linux.
Most of them will work with `ZSH` or `FISH`.
Some of them will not work on `macOS`.

Keybindings are same as `emacs` keybindings since they're both `GNU` program.

## Table of Centents

- [Keybindings](#keybindings)
  - [Navigation](#navigation)
  - [Edit](#edit)
  - [History](#history)
  - [ETC](#etc)

- [VI Motions](#vi-motions)
  - [BASH](#bash)
  - [ZSH](#zsh)

---

## Keybindings

### Navigation

- `ctrl + a` : beginning of the line
- `ctrl + e` : end of the line

- `ctrl + b` : move cursor backward
- `ctrl + f` : move cursor forward

- `alt + b` : move cursor backward by word
- `alt + f` : move cursor forward by word

### Edit

- `ctrl + u` : delete from cursor to start of the line
- `ctrl + k` : delete from cursor to end of the line
- `ctrl + y` : undo

- `ctrl + w` : delete word backward
- `alt + d` : delete word forward

### History

- `ctrl + n` : same as arrow down
- `ctrl + p` : same as arrow up

> Or `!!` to use the last cmd.
> For example:

```sh
sudo !! # last cmd with sudo
```

### ETC

- `alt + period` : use the last argument

> or use `!$` to use the last args

```sh
print !$
```

- `ctrl + l` : same as clear
- `ctrl + d` : same as exit

---

## VI Motions

Use `VI` motions instead of emacs

### BASH

In `~/.bashrc`:

```sh
set -e vi
bind 'set keyseq-timeout 1' # ESC delay to 1ms
```

Or in `~/.inputrc`:

```sh
set keyseq-timeout 1
```

### ZSH

In `~/.zhsrc`:

```sh
bindkey -v
KEYTIMEOUT=1 # ESC delay to 10ms
```
