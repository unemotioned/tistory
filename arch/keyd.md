# Keyd

## Install

```sh
sudo pacman -S keyd
systemctl enable --now keyd
```

## Configure

get device id and input

```sh
keyd monitor
```

keep each conf files per `[ids]`

`/etc/keyd/default.conf`

```conf
[ids]

*

[main]

rightalt = f16
```

```conf
[ids]

# AT Translated Set 2 keyboard
0001:0001:09b4e68d

[main]

rightalt = f16
capslock = overload(control, esc)
esc = capslock
```

```conf

[ids]

# splitkb.com Aurora Sofle v2 rev1
047d:2041:14bbedc4

[main]

rightmouse = mouse1
mouse1 = rightmouse
```

reload after changing

```sh
sudo keyd reload
```
