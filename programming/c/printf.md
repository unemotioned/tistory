# Printf

How to print each data type.

---

## Basic Specifiers

| Type      | Printf       |
| --------- | ------------ |
| short     | `%hd`        |
| int       | `%d` or `%i` |
| long      | `%ld`        |
| long long | `%lld`       |
| char      | `%c`         |
| string    | `%s`         |
| size_t    | `%zu`        |

---

## Float

By default it prints 6 digits after decimal point. Digits after that gets
rounded, not truncated.

| Type        | Printf |
| ----------- | ------ |
| float       | `%f`   |
| double      | `%f`   |
| long double | `%Lf`  |

```c
const float pi = 3.14F;

printf("%.3f\n", pi);
```

### Variable Precision

```c
int precision = 10;

printf("%.*f\n", precision, pi);
```

---

## Unsigned

| Type               | Printf |
| ------------------ | ------ |
| unsigned short     | `%hu`  |
| unsigned int       | `%u`   |
| unsigned long      | `%lu`  |
| unsigned long long | `%llu` |
| unsigned char      | `%hhu` |

### Signed Char

| Type        | Printf |
| ----------- | ------ |
| signed char | `%hhd` |

---

## Pointer

| Type    | Printf |
| ------- | ------ |
| pointer | `%p`   |

By default `%p` prints the address in hex, use `long` to print in decimal.

```c
int x = 10;
int *x_p = &x;

printf("%ld\n", (long)x_p);
```

---

## Non-Decimal

| Type        | Printf       |
| ----------- | ------------ |
| Binary      | `%b`         |
| Octal       | `%o`         |
| Hexadecimal | `%x` or `%X` |

> [!TIP]
> Binary specifier is standardized since C23.
