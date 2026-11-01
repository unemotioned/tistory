# Field Width

Minimum width to print including the text. Does not truncate longer text.

---

## Static

- **Right aligned** (padding before text)

```c
printf("%10s\n", "hello");
```

- **Left aligned** (padding after text)

```c
printf("%-10s\n", "hello");
```

---

## Dynamic

Use `*` to specify field width through an argument.

```c
int width = 20;

printf("%*s\n", width, "world");
printf("%-*s\n", width, "world");
```
