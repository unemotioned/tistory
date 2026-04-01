# Neovim

Build [neovim](https://github.com/neovim/neovim) from source to use the latest
version on Debian/Ubuntu linux

## Table of Contents

- [Dependencies](#dependencies)
- [Build](#build)
- [Update](#update)
- [Uninstall](#uninstall)

---

## Dependencies

- nerd fonts
- ripgrep
- nodejs
- npm
- yarn
  - markdown-preview
- python3-full
  - clang-format
  - pylint
  - isort
  - black
- openjdk-17-jdk
  - nvim-java

```sh
sudo apt install ripgrep nodejs npm python3-full openjdk-17-jdk
```

For the markdown-preview install `yarn` with `npm`

```sh
sudo npm i -g yarn
```

---

## Build

If neovim is already installed with apt, remove before building it.

```sh
sudo apt remove neovim
```

### Prerequisite

```sh
sudo apt install ninja-build gettext cmake curl build-essential git
```

### Clone

```sh
git clone https://github.com/neovim/neovim
cd neovim
```

### Install

```sh
git checkout stable # or nightly
make CMAKE_BUILD_TYPE=RelWithDebInfo
sudo make install
```

Gets installed to `/usr/local`

---

## Update

```sh
cd neovim
git pull
make distclean  # recommended after major updates
make CMAKE_BUILD_TYPE=Release
sudo make install
```

---

## Uninstall

```sh
cd neovim

sudo rm -rf /usr/local/bin/nvim
sudo rm -rf /usr/local/lib/nvim
sudo rm -rf /usr/local/share/nvim
sudo rm -rf /usr/local/lib/cmake/nvim
```
