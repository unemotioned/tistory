# Vim

## Table of Contents

- [Vim Plug](#vim-plug)
- [Fugitive](#fugitive)

---

## Vim Plug

built-in plugin manager

### Install

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

### Usage

add it to `~/.vimrc`

```vim
call plug#begin('~/.vim/plugged')

" for example
Plug 'christoomey/vim-tmux-navigator'

call plug#end()
```

shout out the .`vimrc` and install it

```sh
:source ~/.vimrc # or :so
:PlugInstall
```

---

## Fugitive

```vim
:h fugitive

:h fugitive-maps
```

### Stage

open fugitive window

```vim
:G[it]
```

- `s`: stage
- `u`: unstage
- `-`: stage or unstage
- `U`: unstage all
- `X`: discard under cursor
- `=:` toggle inline diff

### Commit

```vim
:Gcommit
```

- `cc`: create commit
- `ca`: amend last commit
- `cs`: create squash! commit for the commit under the cursor

### Checkout

```vim
:Git checkout <branch-name>
```

- `co<Space>`: populate cmd with `:Git checkout`
- `cb<Space>`: populate cmd with `:Git branch`

### Pull

```vim
:Gpull
```

### Rebase

```vim
:Grebase
```

- `r<Space>`: pouplate cmd with `:Git rebase`

### Merge

```vim
:Gmerge
```

### Push

```vim
:Gpush
```
