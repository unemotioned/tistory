# Vim

## Table of Contents

- [Vim Plug](#vim-plug)
- [Add Plugins](#add-plugins)
- [Install Plugins](#install-plugins)

---

## Vim Plug

Install `vim-plug`

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

---

## Add Plugins

For example add nord theme

```vim
call plug#begin('~/.vim/plugged')

  Plug 'arcticicestudio/nord-vim'

call plug#end()

colorscheme nord
```

---

## Install Plugins

Enter command mode and type:

```sh
PlugInstall
```

---

### Happy Hacking 🎉
