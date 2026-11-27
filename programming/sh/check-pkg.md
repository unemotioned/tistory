# Check Package

```sh
if ! command -Qi nvim &>/dev/null; then
  sudo pacman -S --noconfirm nvim
fi
```

- `&>`: redirect both stdout and stderr
- `/dev/null`: discord output
