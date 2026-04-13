# Vim Motinos

some mesmerizing vim commands worth memorizing

## Table of Contents

- [Stream Editor](#stream-editor)

---

## Stream Editor

> same as `sed` terminal tools

original:

i3 config

```i3
bindsym XF86AudioRaiseVolume exec pactl set-sink-volume @DEFAULT_SINK@ +5%
bindsym XF86AudioLowerVolume exec pactl set-sink-volume @DEFAULT_SINK@ -5%
bindsym XF86AudioMute exec pactl set-sink-volume @DEFAULT_SINK@ toggle
```

converted:

hyprland

```hyprlang
bind = , XF86AudioRaiseVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ +5%
bind = , XF86AudioLowerVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ -5%
bind = , XF86AudioMute, exec, pactl set-sink-volume @DEFAULT_SINK@ toggle
```

the command:

```vim
:s/bindsym \(.*\) exec \(.*\)/bind = , \1, exec, \2/
```

- `:s`: substitute
- `/`: start of search pattern
- `bind = \(.*\) exec`: grab between "bindsym" and "exec" into capture group `\1`
- `\(.*\)`: grab every strings after "exec" to the second capture group `\2`
- `/`: start of replacement
- `bind = , \1`: get the grabbed strings after `bind = ,`
- `, exec, \2`: second grabbed strings after `, exec,`
- `/`: end of command
