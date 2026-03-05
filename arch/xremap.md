# Xremap

Software-level key remapper.

---

## Installation (Hyprland)

```sh
yay -S xremap-wlroots-bin
```

---

## Systemd Service

Create `~/.config/systemd/user/xremap.service`:

```systemd
[Unit]
Description=xremap key remapper
After=graphical-session.target

[Service]
ExecStart=/usr/bin/xremap %h/.config/xremap/config.yml
Restart=on-failure

[Install]
WantedBy=default.target
```

---

## Enable and Start

```sh
systemctl --user enable --now xremap
```

---

### Happy Hacking 🎉
