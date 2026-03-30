# Flameshot

[Flameshot - command line option](https://flameshot.org/docs/advanced/commandline-options/)

---

## Install with APT

```sh
sudo apt install flameshot
```

## Keybind with i3

Example keybind: Alt + Shift + j, k, l

- `gui` : select to capture
- `screen` : selected window
- `full` : entire monitor

Copy to clipboard and save to path

```conf
bindsym Mod1+shift+j exec --no-startup-id flameshot gui --clipboard
bindsym Mod1+shift+k exec --no-startup-id flameshot screen --clipboard --path ~/Pictures/Screenshots
bindsym Mod1+shift+l exec --no-startup-id flameshot full --clipboard --path ~/Pictures/Screenshots
```
