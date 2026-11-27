# Walker

A modern application launcher for Wayland.

## References

- [GitHub](https://github.com/abenz1267/walker)
- [Official Website](https://walkerlauncher.com/)

## Table of Contents

- [Install](#install)
  - [Providers](#providers)
  - [Restart](#restart)
- [Autostart](#autostart)
- [Launch](#launch)
  - [Module](#module)
  - [Keybindings](#keybindings)
- [Prefix](#prefix)

---

## Install

Launcher itself:

```sh
yay -S walker-bin
```

> [!WARNING]
> Do not install `elephant-bin` separately which will cause version mismatch.

### Providers

- [GitHub](https://github.com/abenz1267/walker/#features)

```sh
yay -S \
    elephant-bluetooth \
    elephant-calc \
    elephant-clipboard \
    elephant-symbols \
    elephant-websearch
```

### Restart

Restart `elephant` after installing providers

```sh
pkill elephant
elephant & disown
```

---

## Autostart

Inside `~/.config/hyprland/modules/autostart.lua`:

```lua
hl.on('hyprland.start', function()
  -- ...
  hl.exec_cmd('walker --gapplication-service')
  hl.exec_cmd('elephant')
  -- ...
end)
```

---

## Launch

By terminal commands or with Hyprland keybinds.

### Module

The module name is the string after the semicolon.

```sh
elephant listproviders
```

### Keybindings

Inside `~/.config/hyprland/modules/keybindings.lua`:

```lua
-- default walker
hl.bind(mainMod .. ' + D', hl.dsp.exec_cmd('walker'))

-- clipboard
hl.bind(mainMod .. ' + V', hl.dsp.exec_cmd('walker -m clipboard'))

-- calculator
hl.bind(mainMod .. ' + C', hl.dsp.exec_cmd('walker -m calc'))
```

`-m` is an alias of `--providers`.

---

## Prefix

Use provider after launcher default walker.

- **Calculator**: `=`
- **Clipboard Historyi**: `:`
- **Symbol Pikceri**: `.`
- **Provider Listi**: `;`
- **Websearch**: just search
