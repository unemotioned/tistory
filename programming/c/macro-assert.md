# Macro as Assert

Assert macro to tell assertion has failed from where(file, line) and under what
condition.

---

## Assert

When the `ASSERT_ENABLED` is true(1). If not enabled, do nothing.

```c
#include <stdio.h>
#include <stdlib.h> // exit()

#define ASSERT_ENABLED 1

#if ASSERT_ENABLED
#define ASSERT(c, m)                                                           \
    do {                                                                       \
        if (!(c)) {                                                            \
            fprintf(stderr,                                                    \
                    __FILE__ ": %d: assertion %s failed: %s\n",                \
                    __LINE__,                                                  \
                    #c,                                                        \
                    m);                                                        \
            exit(1);                                                           \
        }                                                                      \
    } while (0)
#else
// do nothing if disabled while keeping the code valid
#define ASSERT(c, m)                                                           \
    do {                                                                       \
    } while (0)
#endif

int main(void) {
    int x = 30;

    ASSERT(x < 20, "x must be under 20");
}
```

**Output**:

```txt
assert.c:22: assertion x < 20 failed: x must be under 20
```

- `__FILE__`, `__LINE__`: Predefined preprocessor macros.
  - `__FILE__ " ... \n"` becomes one string

- `do - while (0)`: Group multiple statements into one. Execute only once since
  it's false.

- `fprintf(stderr, ...)`: Writes formatted output to the stderr stream.

- `#c`: **Stringification** of arg c. `x < 20` into literal string.
