# GTK Theme

Apply a GTK theme to applications like `Nautilus` on Hyprland

---

## Installation

```sh
yay -S catppuccin-gtk-theme-mocha
```

---

## Configuration

### Find Name

```sh
ls /usr/share/themes | grep -i catppuccin
```

### Set Theme

inside the `~/.config/hypr/hyprland.conf`

```hyprlang
env = GTK_THEME,catppuccin-mocha-pink-standard+default
```

---

## Unset

To revert to the default theme:

1. Comment out the `GTK_THEME` line in `hyprland.conf`
2. Log out and log back in

The theme will fall back to `Adwaita`
