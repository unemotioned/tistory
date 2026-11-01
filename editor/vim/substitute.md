# Substitute

Original:

```sh
# i3wm config
bindsym XF86AudioRaiseVolume exec pactl set-sink-volume @DEFAULT_SINK@ +5%
bindsym XF86AudioLowerVolume exec pactl set-sink-volume @DEFAULT_SINK@ -5%
bindsym XF86AudioMute exec pactl set-sink-volume @DEFAULT_SINK@ toggle
```

Converted:

```hyprlang
# hyprland config
bind = ,XF86AudioRaiseVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ +5%
bind = ,XF86AudioLowerVolume, exec, pactl set-sink-volume @DEFAULT_SINK@ -5%
bind = ,XF86AudioMute, exec, pactl set-sink-volume @DEFAULT_SINK@ toggle
```

The command:

```vim
:s/bindsym \(.*\) exec \(.*\)/bind = ,\1, exec,\2/
```

| Elements             | Explanation                                           |
| -------------------- | ----------------------------------------------------- |
| `:s`                 | substitute                                            |
| `/`                  | start of search pattern                               |
| `bind = \(.*\) exec` | between "bindsym" and "exec" into capture group `\1`  |
| `\(.*\)`             | strings after "exec" to the second capture group `\2` |
| `/`                  | start of replacement                                  |
| `bind = , \1`        | capture group 1 after `bind = ,`                      |
| `, exec, \2`         | capture group 2 after `, exec,`                       |
| `/`                  | end of command                                        |
