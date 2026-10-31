# Field Width

Minimum width to print including the text. Does not truncate longer text.

- right aligned (padding before text)

```c
printf("%10s\n", "hello");
```

- left aligned (padding after text)

```c
printf("%-10s\n", "hello");
```

---

## Dynamic Field Width

use `*` to specify field width through args

```c
int width = 20;

printf("%*s\n", width, "world");
printf("%-*s\n", width, "world");
```
