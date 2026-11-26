# Reflector

Mirror list manager.

## Reference

- [ArchWiki](https://wiki.archlinux.org/title/Reflector)

## Table of Contents

- [Install](#install)
- [Update Mirror List](#update-mirror-list)
- [Timer](#timer)
  - [Add Schedule](#add-schedule)
  - [Check Schedule](#check-schedule)
  - [Validate Timer](#validate-timer)
  - [Edit Arguments](#edit-arguments)

---

## Install

```sh
sudo pacman -Syu reflector
```

```sh
reflector --version
```

---

## Update Mirror List

```sh
sudo reflector \
    --save /etc/pacman.d/mirrorlist \
    --protocol https \
    --country KR,JP \
    --latest 10 \
    --sort rate \
    --verbose
```

- `--sort rate`: sort by download speed

---

## Timer

### Add Schedule

```sh
sudo systemctl edit reflector.timer
```

Add:

```text
[Timer]
OnCalendar=
OnCalendar=weekly
OnBootSec=15min
RandomizedDelaySec=0
Persistent=false
```

- sort mirrors weekly
- 15 minutes after boot

Apply timer:

```sh
sudo systemctl daemon-reload
sudo systemctl enable reflector.timer
sudo systemctl restart reflector.timer
```

### Check Schedule

```sh
systemctl list-timers reflector.timer
```

### Validate Timer

```sh
sudo systemd-analyze verify reflector.timer
```

- No output means nothing wrong.

### Edit Arguments

Reflecotr arguments to run on scheduled time.

Edit arguments inside `/etc/xdg/reflector/reflector.conf` to match command from
[udpate mirror list](#update-mirror-list).
