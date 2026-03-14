# Fix Kitty

---

## Problem

Warning: `org.freedesktop.portal.Settings` not found

---

## Solution

Install portals:

```sh
sudo pacman -S xdg-desktop-portal xdg-desktop-portal-gtk xdg-desktop-portal-hyprland
```

Start and restart services:

```sh
systemctl --user enable --now xdg-desktop-portal xdg-desktop-portal-gtk xdg-desktop-portal-hyprland
```

Set `/usr/share/xdg-desktop-portal/hyprland-portals.conf`:

```ini
[preferred]
default=hyprland;gtk
```
