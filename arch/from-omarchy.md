# From Omarchy

## impla

dependencies: iwd

TUI network manager

```sh
sudo pacman -S impala iwd
```

```sh
impala
```

---

## bluetui

TUI bluetooth manager

```sh
sudo pacman -S bluetui
```

```sh
bluetui
```

---

## pinta

Painting made simple

---

## localsend

file sharing in LAN

```sh
yay -S localsend-bin
```

---

## hyprmon

monitor profile tui

```sh
yay -S hyprmon-bin
```

---

## github-cli

you can pull push private repo with the http without ssh key

```sh
sudo pacman -S github-cli
```

start

```sh
gh auth login
```

clone with user and repo name

```sh
gh repo clone UnEmotioneD/tistory
```

clone with URL

```sh
gh repo clone https://github.com/UnEmotioneD/tistory
```

```sh
gh auth status
```

## satty

modern screenshot tool

```sh
sudo pacman -S satty
```

- `slurp`: selection ui
- `grim`: get image from slurp
- `satty`: annotation tool

```hyprlang
bind = ALT SHIFT, J, exec, grim -g "$(slurp)" - | satty --filename - --early-exit
```

<!-- TODO: -->

- save to `~/Pictures/Screenshots`
- name automatically
- close on copy or save

- screenshot selected
- screenshot selected window
- screenshot selected output
