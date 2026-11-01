# Vim Plug

Built-in plugin manager.

---

## Install

Install vim-plug at `~/.vim/autoload/plug.vim`:

```sh
curl -fLo \
  ~/.vim/autoload/plug.vim --create-dirs \
  https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

---

## Usage

Add it to `~/.vimrc`:

```vim
call plug#begin('~/.vim/plugged')

" for example
Plug 'christoomey/vim-tmux-navigator'

call plug#end()
```

Source `.vimrc` and install:

```sh
:source ~/.vimrc # or :so
:PlugInstall
```
