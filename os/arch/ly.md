# LY

Minimal display manager.

## Reference

- [GitHub](https://github.com/fairyglade/ly)

---

## Install

```sh
sudo pacman -S ly
yay -S durdraw  # for animation only
```

---

## Usage

Enable `ly` and disable `getty` from **tty2**:

```sh
sudo systemctl enable ly@tty2.service
sudo systemctl disable getty@tty2.service
```

Disable previous display manager:

```sh
sudo systemctl disable sddm
sudo systemctl disable getty@tty1.service
```

---

## Configure

Inside `/etc/ly/config.ini`:

```dosini
# Erase password input on failure
clear_password = false
```

Change this to `true`.
