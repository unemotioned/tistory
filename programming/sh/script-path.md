# Script Path

1. get parent directory of script file
2. move into it
3. assign its path into variable

```sh
SCRIPT_DIR="$(cd "$(dirname "${BASH_SOURCE[0]}")" && pwd)"
```

- `BASH_SOURCE[0]`: BASH variable that holds path of current script file
  - `$0`: does not point to file when it's `sourced`
