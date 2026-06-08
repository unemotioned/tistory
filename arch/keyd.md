# Keyd

## Install

```sh
sudo pacman -S keyd
systemctl enable --now keyd
```

## Configure

get device id and input

```sh
sudo keyd monitor
```

> **_Important:_** Get the device ID fro the same line as `device add:` not from the `keyd virtual keyboard` when you type the keys.

> **_NOTE:_** The device ID might change after kernel update

keep each conf files per `[ids]`

`/etc/keyd/builtin.conf`

```conf
[ids]

*

[main]

rightalt = f16
```

```conf
[ids]

# AT Translated Set 2 keyboard
0001:0001:3cf016cc

[main]

rightalt = f16
capslock = overload(control, esc)
esc = capslock
```

```conf

[ids]

# Kensington Slimblade Trackball
047d:2041:14bbedc4

[main]

rightmouse = mouse1
mouse1 = rightmouse
```

reload after changing

```sh
sudo keyd reload
```
