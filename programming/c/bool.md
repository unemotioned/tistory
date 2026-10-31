# Boolean

```c
#include <stdbool.h>
```

- false: 0
- true: anything else then 0, but 1 conventionally

```c
#include <stdbool.h>
#include <stdio.h>

int main(void) {
    if (1) {
        printf("Yay!\n");
    }

    bool im_ready = true;

    if (im_ready) {
        printf("Hello, World!\n");
    } else {
        printf("Foobar\n");
    }

    return 0;
}
```
