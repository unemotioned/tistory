# Struct

Something close to **class** in objective programming.

---

- Don't forget the semi-colon at the end of declaration
- Variable not initialized will automatically be assigned with value of `0`

```c
#include <stdio.h>

struct foo {
    float x;
    float y;
};

int main(void) {
    struct foo foo = {
        // .x = 1.0f, // 0 by default if not assigned
        .y = 2.0f,
    };

    printf("foo = < %f, %f >\n", foo.x, foo.y);

    foo.x = 1.0f;
    foo.y = 3.0f;

    printf("foo = < %f, %f >\n", foo.x, foo.y);


    return 0;
}
```

## Typedef

Use `typedef` to later declare struct without the struct keyword.

```c
#include <stdio.h>

// With `typedef`, name of the struct must come after brace.
// Define anonymous struct and give `bar` alias.
typedef struct {
    int v;
    int w;
} bar;

int main(void) {
    bar bar = {
        .v = 4,
        .w = 5,
    };

    printf("bar = < %d, %d >\n", bar.v, bar.w);

    return 0;
}
```
