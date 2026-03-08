# Clipboard History

## Install

```sh
yay -S cliphist
```

## Start

```hyprlang
exec-once = wl-paste --watch cliphist store
```

## Usage

```hyprlang
bind = $mainMod, V, exec, cliphist list | wofi --dmenu --lines=10 | cliphist decode | wl-copy
```

1. open cllipboard history with wofi
2. search
3. select
4. paste it to where you want
