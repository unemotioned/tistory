# Type

---

## Declarations

### Integers

```c
int i32 = 4;

long i64 = 8;

long long i64 = 16;

short i16 = -2;
```

Check out [typedef.md](./typedef.md) for using guaranteed size of integers.

### Float

```c
float f = 0.0F;
double d = 0.0;
long double ld = 0.0L;
```

Check out [float.md](./float.md) for more.

### Pointer

```c
int x = 10;

int *x_p = &x;

int **x_pp = &x_p; // pointer to a pointer
```

Some formatting styles put `*` next to type keyword.

```c
int* x_ptr = &x;
```

### Array

```c
int arr_1[5] = {0}; // all five elements are initialized to zero

int arr_2[] = {1, 2, 3, 4, 5}; // length is inferred from the initializer
```

### String

```c
const char *s1 = "string as pointer";

char s2[] = "string as char arr";
```

Check out [string.md](./string.md) for more.

### size_t

Result of the `sizeof` operator.

Can be `unsigned int` or `unsigned long` or `unsigned long long`.

```c
#include <stddef.h>

int arr[5] = {0};
size_t size = sizeof(arr); // total size of the array in bytes
```

---

## Sizes

1 byte = 8 bits

| Type        | Typical size (bytes) |
| ----------- | -------------------- |
| char        | `1`                  |
| short       | `2`                  |
| int         | `4`                  |
| long        | `4` or `8`           |
| long long   | `8`                  |
| float       | `4`                  |
| double      | `8`                  |
| long double | `8` or `12` or `16`  |
| size_t      | `4` or `8`           |
| pointer     | `4` or `8`           |

On a 32-bit architecture, pointers are 32 bits wide.

---

## Minimum and Maximum Values

`n`: The number of bits in the data type.

**Minimum**:

```math
-1 \times ( 2 ^ { n - 1 } )
```

**Maximum**:

```math
2 ^ { n - 1 } - 1
```

---

## Signedness

The most significant bit (MSB) of a signed integer indicates whether its value
is negative or non-negative (including zero).

```c
unsigned int ui = 10;

unsigned short us = 20;

unsigned long ul = 30;

unsigned char uc = 'c';

signed char sc = -1;
```

- `unsigned char`: Raw bytes, such as image data or file contents.
- `signed char`: Small integers that may be negative.

> [!NOTE]
> Whether plain `char` is signed or unsigned is **implementation-defined**.
> Do not assume it can represent negative values or values greater than 127.

Unsigned integer types represent non-negative values.

For the same width, the maximum unsigned value is about twice the maximum signed
value.

```math
2 ^ n - 1
```
