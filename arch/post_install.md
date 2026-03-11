# After installing Arch linux

[10 things you must do after installing arch linux by Ksk Royal](https://www.youtube.com/watch?v=odgD_RdJjCU)

## Table of Contents

- [Pacman](#pacman)
  - [Configure](#configure)
  - [Increaase Download Speed](#increase-download-speed)
- [Additional Kernel](#additional-kernel)
- [Timeshift](#timeshift)

---

## Pacman

### Configure

Open /etc/pacman.conf with sudo previliages

```sh
sudo nvim /etc/pacman.conf
```

Under `[options]` and `# Misc options` uncomment `Color`

Add `ILoveCandy` to make the download progress bar to look like the pacman game

and update the pacman

```sh
sudo pacman -Sy
```

### Increase Download Speed

Install `reflector` with pacman

```sh
sudo pacman -S reflector
```

Create backup of default mirror list

```sh
sudo cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
```

then fetch the top 10 fastest servers

```sh
sudo reflector --verbose --latest 10 --protocol https --sort rate --save /etc/pacman.d/mirrorlist
```

and update the pacman again

---

## Additional Kernel

Install LTS as backup:

```sh
sudo pacman -S linux-lts linux-lts-headers
```

Update GURB config:

```sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

---

## Timeshift

linux backup system

```sh
sudo pacman -S timeshit
```

```sh
sudo timeshift --check
```

this will create snapshot
