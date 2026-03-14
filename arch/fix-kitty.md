# Fix Kitty

---

## Problem

Warning: `org.freedesktop.portal.Settings` not found

---

## Solution

Install portals:

```sh
sudo pacman -S xdg-desktop-portal-gtk xdg-desktop-portal-hyprland
```

Start and restart services:

```sh
systemctl --user start xdg-desktop-portal-gtk
systemctl --user restart xdg-desktop-portal xdg-desktop-portal-hyprland xdg-desktop-portal-gtk
```

Set `/usr/share/xdg-desktop-portal/hyprland-portals.conf`:

```ini
[preferred]
default=hyprland;gtk
```
