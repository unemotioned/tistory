# Z-Shell

Larger ecosystem and better customizability then BASH

---

## Prerequist

### Install Git

For cloning plugins

```sh
sudo apt install git
git --version
```

---

## ZSH

### Install ZSH

```sh
sudo apt install zsh
```

### Change Shell

```sh
chsh -s $(which zsh)
```

Reboot needed

---

## Plugins

### [Oh My ZSH](https://ohmyz.sh/#install)

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### [Powerlevel10k](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#manual)

```sh
git clone https://github.com/romkatv/powerlevel10k.git ~/.oh-my-zsh/custom/themes/powerlevel10k
```

### [ZSH-Autosuggestions](https://github.com/zsh-users/zsh-history-substring-search)

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
```

### [ZSH-History-Substring-Search](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)

```sh
git clone https://github.com/zsh-users/zsh-history-substring-search ~/.oh-my-zsh/custom/plugins/zsh-history-substring-search
```

### [Fast-syntax-highlighting](https://github.com/zdharma-continuum/fast-syntax-highlighting?tab=readme-ov-file#installation)

```sh
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/fast-syntax-highlighting
```

---

## Tools

### [FZF](https://github.com/junegunn/fzf?tab=readme-ov-file#using-git)

Download and install from source instead of using `apt`

```sh
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

Install `fdfind`(fd) to use with `Fzf`

```sh
sudo apt install fdfind
```

### [FZF-git](https://github.com/junegunn/fzf-git.sh?tab=readme-ov-file)

Used by `nvim` but sourced from `~/.zshrc`

```sh
git clone https://github.com/junegunn/fzf-git.sh.git
```

Source it from `~/.zshrc`
