# Keyd

Remap laptop's builtin keyboard and trackball's buttons with
[keyd](https://github.com/rvaiya/keyd).

---

## Install

```sh
sudo pacman -S keyd
systemctl enable --now keyd
```

---

## Configure

Get device ID and input:

```sh
sudo keyd monitor
```

> [!IMPORTANT]
> Get the `device ID` from the same line as `device add:`, **_NOT_** from
> `keyd virtual keyboard` when you press the keys.

Keep each conf file per `[ids]`.

Remap for all `/etc/keyd/all.conf`:

```conf
[ids]

*

[main]

rightalt = f16
```

Remap Built-in Thinkpad keyboard `/etc/keyd/kb.conf`:

```conf
[ids]

# AT Translated Set 2 keyboard
0001:0001:09b4e68d

[main]

rightalt = f16
capslock = overload(control, esc)
esc = capslock
```

> [!IMPORTANT]
> `rightalt = f16` is duplicated but must be set separately.

Remap Trackball `/etc/keyd/ball.conf`:

```conf
[ids]

# Kensington Slimblade Trackball
047d:2041:14bbedc4

[main]

rightmouse = mouse1
mouse1 = rightmouse
```

---

## Reload

```sh
sudo keyd reload
```
