# Printf

---

## Basic

| Type        | Printf       |
| ----------- | ------------ |
| short       | `%hd`        |
| int         | `%d` or `%i` |
| long        | `%ld`        |
| long long   | `%lld`       |
| float       | `%f`         |
| double      | `%f`         |
| long double | `%Lf`        |
| character   | `%c`         |
| string      | `%s`         |
| size_t      | `%zu`        |
| pointer     | `%p`         |

> [!IMPORTANT]
> if `float` is not initialized with **f** at the end of literal it will implicitly
> converted to `double`

---

## Unsigned

| Type               | Printf |
| ------------------ | ------ |
| unsigned short     | `%hu`  |
| unsigned int       | `%u`   |
| unsigned long      | `%lu`  |
| unsigned long long | `%llu` |
| signed char        | `%hhd` |
| unsigned char      | `%hhu` |

---

## Others

| Type        | Printf       |
| ----------- | ------------ |
| Hexadecimal | `%x` or `%X` |
| Octal       | `%0`         |
