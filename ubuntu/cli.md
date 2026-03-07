# CLI Tools

- Command Line Interface

## List of cli-tools

- git
- curl
- stow
- [tmux](#tmux)
- [bat](#bat)
- [eza](#eza)
- [zoxide](#zoxide)
- [yazi](#yazi)
- [lazygit](#lazygit)
- [delta](#delta)
- [fastfetch](#fastfetch)
- pavucontrol

---

APT installable packages

```sh
sudo apt install git curl stow tmux bat eza zoxide git-delta pavucontrol
```

---

## TMUX

Terminal Multi Plexer

Clone TPM(tmux plugins manager) for use

`~/.tmux/plugins`: where plugins will be installed

```sh
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

- Inside tmux session `prefix + I` to install plugins.
- `prefix + U` to update plugins.

---

## Bat

Better file previewer

### Install Bat

```sh
sudo apt install bat
```

### Create Bat Theme Directory

```sh
mkdir -p "$(bat --config-dir)/themes" # ~/.config/bat/themes
cd "$(bat --config-dir)/themes"
```

### Install Bat Theme

From the themes directory download a theme

- `tokyonight_storm` theme for sublime

```sh
curl -O https://raw.githubusercontent.com/folke/tokyonight.nvim/main/extras/sublime/tokyonight_storm.tmTheme
```

### Use Bat

Inside `.bashrc` or `.zshrc` set bat to use installed theme

```sh
export BAT_THEME=tokyonight_storm
```

Additionally set alias:

```sh
alias bat='batcat'
```

Create cache to use the theme:

```sh
bat cache --build
```

Test it:

```sh
bat ~/.bashrc
```

---

## Eza

- [eza - github](https://github.com/eza-community/eza)

`ls` command replcement

add the following alias to `.bashrc` or `.zshrc`

- list in vertical line
- color and icons
- directory first
- show git status

```sh
alias ls="eza --oneline --color=always --icons=always --group-directories-first --git"
```

---

## Zoxide

- [zoxide - github/installation](https://github.com/ajeetdsouza/zoxide?tab=readme-ov-file#installation)

better `cd`

load `zoxide` and override `cd` to use zoxide

- Bash

```sh
eval "$(zoxide init --cmd cd bash)"
```

- ZSH

```sh
eval "$(zoxide init --cmd cd zsh)"
```

---

## Lazygit

Git TUI(Terminal User Interface) wrapper

[lazygit github/install ubuntu](https://github.com/jesseduffield/lazygit?tab=readme-ov-file#debian-and-ubuntu)

### Install LazyGit

```bash
LAZYGIT_VERSION=$(curl -s "https://api.github.com/repos/jesseduffield/lazygit/releases/latest" | \grep -Po '"tag_name": *"v\K[^"]*')
curl -Lo lazygit.tar.gz "https://github.com/jesseduffield/lazygit/releases/download/v${LAZYGIT_VERSION}/lazygit_${LAZYGIT_VERSION}_Linux_x86_64.tar.gz"
tar xf lazygit.tar.gz lazygit
sudo install lazygit -D -t /usr/local/bin/
```

Remove temp files after install:

```sh
rm ~/lazygit ~/lazygit.tar.gz
```

### Update Lazygit

To update remove lazygit at `/usr/local/bin` and run the install scripts again

```sh
sudo rm /usr/local/bin/lazygit
```

### Configure

Config file path: `~/.config/lazygit/config.yml`

Border corner 90 degree:

```yml
gui:
  border: single
```

---

## Yazi

- [yazi install ubuntu](https://yazi-rs.github.io/docs/installation#debian)

terminal file explorer

### Prerequist

```sh
sudo apt install ffmpeg 7zip jq poppler-utils fd-find ripgrep zoxide imagemagick build-essential
```

### Setup Cargo

- [Install Rust](https://rust-lang.org/tools/install/)

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup update
```

### Clone and Build

```sh
git clone https://github.com/sxyazi/yazi.git
cd yazi
cargo build --release --locked
```

and move `yazi`, `ya` files to `$PATH`

```sh
sudo mv target/release/yazi target/release/ya /usr/local/bin/
```

### Yazi Theme

Add tokyonight theme with yazi package manager `ya`:

```sh
ya pkg add BennyOe/tokyo-night
```

This will create `flavors/` under yazi config directory,
you only need `flavors.toml` and `tmtheme.xml` files

Under the `~/.config/yazi` add `theme.toml` file, inside:

```toml
[flavor]
use = "tokyo-night"
# For Yazi 0.4 and above
dark = "tokyo-night"
```

### Update

1. pull latest update
2. update `cargo`
3. build with `cargo`
4. move `yazi` and `ya` to `$PATH`

### Uninstall Yazi

Remove the `yazi` and `ya` files under the `$PATH`

```sh
sudo rm /usr/local/bin/yazi /usr/local/bin/ya
```

Then remove the cloned repo

---

## Delta

[delta / GitHub](https://github.com/dandavison/delta)

add the following to `~/.gitconfig` customize `delta`

```gitconfig
[core]
  pager = delta
[interactive]
  diffFilter = delta --color-only
[delta]
  # use n / N to move between diff sections
  navigate = true
  side-by-side = true
  line-numbers = true
  syntax-theme = Visual Studio Dark+
[merge]
  conflictstyle = zdiff3
[diff]
  colorMoved = default
```

---

## Fastfetch

System info fetch program

### Install with PPA

```sh
sudo add-apt-repository ppa:zhangsongcui3371/fastfetch
sudo apt upgrade
sudo apt install fastfetch
```

### Uninstall

```sh
sudo apt remove fastfetch
sudo add-apt-repository --remove ppa:zhangsongcui3371/fastfetch
```
