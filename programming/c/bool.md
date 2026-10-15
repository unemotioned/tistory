# Boolean

`0` equals **false** and anything else equals **true** but `1` conventionally

```c
#include <stdbool.h>
```

---

```c
#include <stdbool.h>
#include <stdio.h>

int main() {
    if (1) {
        printf("yay\n");
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
