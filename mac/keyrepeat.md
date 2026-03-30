# macOS Key Repeat Configuration

Override the default keyboard repeat behavior in macOS to achieve faster,
more responsive key repetition.

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

| Value | Time     |
| ----- | -------- |
| 10    | ~183 ms  |
| 15    | ~267 ms  |
| 30    | ~517 ms  |
| 120   | ~2017 ms |

### KeyRepeat (Delay Between Each Repeat)

**Formula:** `time (ms) = value × 15 ms`

| Value | Time    |
| ----- | ------- |
| 1     | 15 ms   |
| 2     | 30 ms   |
| 6     | 90 ms   |
| 120   | 1800 ms |

---

## Reverting to Defaults

To restore macOS defaults:

```sh
defaults delete -g InitialKeyRepeat
defaults delete -g KeyRepeat
```

Then log out and back in.

---

## Checking Current Values

```sh
# Check current InitialKeyRepeat
defaults read -g InitialKeyRepeat

# Check current KeyRepeat
defaults read -g KeyRepeat
```
