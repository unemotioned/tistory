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

```ini
[Unit]
Description=xremap key remapper
After=graphical-session.target

[Service]
# --device: explicitly include pointer devices (auto-detection only picks keyboards)
ExecStart=/usr/bin/xremap --device "Kensington Slimblade Trackball" %h/.config/xremap/config.yml
Restart=on-failure

[Install]
WantedBy=default.target
```

---

## Enable and Start

```sh
systemctl --user enable --now xremap
```
