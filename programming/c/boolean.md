# Boolean

Using **Boolean** type in C.

---

**Include**:

```c
#include <stdbool.h>
```

- `false`: 0
- `true`: Anything else then 0, but 1 conventionally.

```c
bool im_ready = true;

if (im_ready) {
    printf("I'm ready\n");
} else {
    printf("I'm NOT ready\n");
}

printf("size of bool: %zu\n", sizeof(bool)); // 1
```

- `sizeof(bool)`: 1 Byte == 8 Bits
