# Audio

## Install

`pipewire-audio` includes pipewire, pipewire-pulse and wireplumber

```sh
sudo pacman -Syu pipewire-audio pavucontrol
```

audio output via thunderbolt:

```sh
sudo pacman -Syu bolt
```

---

## Enable Service

```sh
systemctl --user enable pipewire pipewire-pulse wireplumber
```
