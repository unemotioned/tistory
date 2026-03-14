# Grep

## Find String Inside Files

```sh
grep -r "<string>" .
```

| Option                         | Description                |
| ------------------------------ | -------------------------- |
| `-r`                           | Recursive search           |
| `-i`                           | Case-insensitive           |
| `-n`                           | Show line numbers          |
| `-l`                           | Show only filenames        |
| `--binary-files=without-match` | Exclude binary files       |
| `--include="*.txt"`            | Search specific file types |
| `--exclude-dir=node_modules`   | Exclude a directory        |

### Examples

```sh
# Case-insensitive search
grep -ri "<string>" .

# Show line numbers
grep -rn "<string>" .

# Show only filenames (no content)
grep -rl "<string>" .

# Show filename + line number + content
grep -rn "<string>" .

# Exclude binary files
grep -r "<string>" . --binary-files=without-match

# Search only specific file types (e.g. .txt, .conf)
grep -r "<string>" . --include="*.txt"

# Exclude a directory (e.g. node_modules)
grep -r "<string>" . --exclude-dir=node_modules
```
