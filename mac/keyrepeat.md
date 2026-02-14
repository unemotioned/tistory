# macOS Key Repeat Configuration

Override the default keyboard repeat behavior in macOS to achieve faster, more responsive key repetition.

## Quick Start

```sh
# Set delay before repeat starts (lower = faster)
defaults write -g InitialKeyRepeat -int 10

# Set delay between each repeat (lower = faster)
defaults write -g KeyRepeat -int 1
```

**Important:** Log out and back in for changes to take effect.

---

## Understanding the Values

### InitialKeyRepeat (Delay Before Repeat Starts)

**Formula:** `time (ms) = (value + 1) × 16.67 ms`

| Value | Time     | Description            |
| ----- | -------- | ---------------------- |
| 10    | ~183 ms  | Very responsive        |
| 15    | ~267 ms  | macOS minimum (via UI) |
| 30    | ~517 ms  | Half a second          |
| 120   | ~2017 ms | macOS default          |

### KeyRepeat (Delay Between Each Repeat)

**Formula:** `time (ms) = value × 15 ms`

| Value | Time    | Description            |
| ----- | ------- | ---------------------- |
| 1     | 15 ms   | Extremely fast         |
| 2     | 30 ms   | macOS minimum (via UI) |
| 6     | 90 ms   | Balanced               |
| 120   | 1800 ms | macOS default          |

---

## Recommended Presets

### Ultra Fast (for power users)

```sh
defaults write -g InitialKeyRepeat -int 10
defaults write -g KeyRepeat -int 1
```

### Fast but Controlled

```sh
defaults write -g InitialKeyRepeat -int 15
defaults write -g KeyRepeat -int 2
```

### Balanced

```sh
defaults write -g InitialKeyRepeat -int 20
defaults write -g KeyRepeat -int 4
```

---

## Reverting to Defaults

To restore macOS defaults:

```sh
defaults delete -g InitialKeyRepeat
defaults delete -g KeyRepeat
```

Then log out and back in.

---

## Tips

- Start with moderate values and adjust based on your preference
- Values that are too low may cause unintended repeated characters
- Different keyboards may feel different with the same settings
- These settings affect all applications system-wide

---

## Checking Current Values

```sh
# Check current InitialKeyRepeat
defaults read -g InitialKeyRepeat

# Check current KeyRepeat
defaults read -g KeyRepeat
```
