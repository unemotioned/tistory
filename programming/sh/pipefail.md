# Pipefail

Script error handling.

```sh
#!/usr/bin/env bash
set -euo pipefail
```

| Flag       | Meaning                                     |
| ---------- | ------------------------------------------- |
| `-e`       | Exit immediately if a command fails         |
| `-u`       | Treat unset variables as errors             |
| `-o`       | Set a named option                          |
| `pipefail` | Pipe fails if any command in the pipe fails |
