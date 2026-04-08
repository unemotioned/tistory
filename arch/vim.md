# Vim

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
