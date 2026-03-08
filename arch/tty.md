# TeleTypeWriter

What it is:

- Originally physical typewriter terminals connected to computers
- Now virtual consoles built into Linux that provide a basic text interface
- Completely separate from your graphical desktop

---

When/Why to use it:

| When                              | Why                                  |
| --------------------------------- | ------------------------------------ |
| Graphical session crashes/freezes | Fix it from TTY                      |
| Hyprland/Wayland won't start      | Debug from TTY without a GUI         |
| Display manager broken            | Log in and fix configs from TTY      |
| Running heavy tasks               | Avoid overhead of GUI                |
| System maintenance                | pacman updates, editing config files |
| No GUI available                  | Servers, minimal installs            |

## Keyboard Shortcut

Ctrl + Alt + F1 ~ F7

## Terminal Command

switch to TTY2:

```sh
chvt 2
```

## TTY 1 through 7

In hyprland:

1. Default
2. Show SDDM login screen and no input is working
3. 3 through 7 works fine
