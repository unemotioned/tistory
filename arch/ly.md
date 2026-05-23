# LY

[GitHub - fairyglade/ly](https://github.com/fairyglade/ly)

Minimal display manager

---

## Install

```sh
sudo pacman -S ly
yay -S durdraw  # for animation
```

---

## Usage

Enable `ly` and disable `getty` from tty 2

```sh
sudo systemctl enable ly@tty2.service
sudo systemctl disable getty@tty2.service
```

```sh
sudo systemctl disable sddm
sudo systemctl disable getty@tty1.service
```
