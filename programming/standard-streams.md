# Standard Streams

Default channels a program uses to receive input, produce output and report
errors. That can be redirected to fies or other programs.

---

## Streams

| Stream   | File Descriptor | Purpose                |
| -------- | --------------- | ---------------------- |
| `stdin`  | 0               | Receives input         |
| `stdout` | 1               | Displays output        |
| `stderr` | 2               | Displays error message |

---

## File Descriptor

File descriptors 0, 1 and 2 is reserved as POSIX convention.

```c
#include <fcntl.h>
#include <stdio.h>
#include <unistd.h>

int main(void) {
    int fd = open("foo.txt", O_RDONLY);

    printf("File descriptor: %d\n", fd);

    close(fd);

    return 0;
}
```

Result:

```txt
File descriptor: 3
```

---

## Redirection Operator

| Operator | Meaning                                        | Example                  |
| -------- | ---------------------------------------------- | ------------------------ |
| `<`      | stdin from file                                | `cat < input.txt`        |
| `>`      | stdout to file                                 | `ls > input.txt`         |
| `2>`     | stderr to file                                 | `ls 2> error.txt`        |
| `&>`     | stdout and stderr to file                      | `&>/dev/null`            |
| `>>`     | append stdout to file                          | `echo hi >> log.txt`     |
| `2>>`    | append stderr to file                          | `ls bad 2>> error.txt`   |
| `2>&1`   | redirect stderr to where stdout currently goes | `command > all.txt 2>&1` |
| `\|`     | pipe stdout into another command's stdin       | `ls \| grep txt`         |

### Redirect Output

```sh
./foobar > output.txt 2> error.txt
```

- `printf()` messages are written to `output.txt`
- `fprintf()` messages are written to `error.txt`
