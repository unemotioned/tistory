# Lazygit

Git TUI(Terminal User Interface) wrapper

[lazygit github/install ubuntu](https://github.com/jesseduffield/lazygit?tab=readme-ov-file#debian-and-ubuntu)

---

## Install

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

---

## Update

To update remove lazygit at `/usr/local/bin` and run the install scripts again

```sh
sudo rm /usr/local/bin/lazygit
```

---

## Configure

Config file path: `~/.config/lazygit/config.yml`

Border corner 90 degree:

```yml
gui:
  border: single
```
