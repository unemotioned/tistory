# After installing Arch linux

[10 things you must do after installing arch linux by Ksk Royal](https://www.youtube.com/watch?v=odgD_RdJjCU)

## Table of Contents

- [Pacman](#pacman)
  - [Configure](#configure)
  - [Increase Download Speed](#increase-download-speed)
- [Additional Kernel](#additional-kernel)
- [Timeshift](#timeshift)
  - [grub-btrfs](#grub-btrfs)
  - [inotify-tools](#inotify-tools)
  - [Enable grub-btrfsd](#enable-grub-btrfsd)
  - [Testing](#testing)
  - [timeshift-autosnap](#timeshift-autosnap)

---

## Pacman

### Configure

Open `/etc/pacman.conf` with sudo privileges

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

Update GRUB config:

```sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```

---

## Timeshift

> need btrfs formatted partition and subvolumes

linux backup system

```sh
sudo pacman -S timeshift
```

```sh
sudo timeshift --check
```

this will create snapshot

```sh
sudo pacman -S grub-btrfs
```

### grub-btrfs

```sh
sudo bash /etc/grub.d/41_snapshots-btrfs
```

### inotify-tools

update grub snapshot when new snapshot is created

```sh
yay -S inotify-tools
```

```sh
sudo systemctl edit --full grub-btrfsd
```

```ini
# from this
ExecStart=/usr/bin/grub-btrfsd --syslog /snapper
# to this
ExecStart=/usr/bin/grub-btrfsd --timeshift-auto
```

### Enable grub-btrfsd

```sh
sudo systemctl enable --now grub-btrfsd
```

### Testing

from terminal to see what is going on

```sh
journalctl -f
```

1. open timeshift
2. create new snapshot
3. check it is working from the log

### timeshift-autosnap

```sh
yay -S timeshift-autosnap
```

```sh
sudo -E nvim /etc/timeshift-autosnap.conf
```
