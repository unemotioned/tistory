# Exit Codes

`0 ~ 255`: Any none-zero value signals an error.

| Code  | Meaning                       |
| ----- | ----------------------------- |
| `0`   | Success                       |
| `1`   | General error                 |
| `2`   | misuse of shell builtins      |
| `126` | Cmd found but not executable  |
| `127` | Cmd not found                 |
| `130` | Script terminated by `Ctrl+C` |
