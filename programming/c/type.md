# Type

min max value it can store

how to print them

type conversion

binary and hex

what is size_t

sizeof()

---

## Variables

### Basic

```c
int a = 0;

float b = 3.14f;

double c = 3.14159;

char d = 'c';

char e[] = "string literal";
```

### Size

1 Byte == 8 Bit

| Type        | Size (Byte) |
| ----------- | ----------- |
| `char`      | 1           |
| `short`     | 2           |
| `int`       | 4           |
| `long`      | 4 or 8      |
| `long long` | 8           |
| `float`     | 4           |
| `double`    | 8           |

### Min Max

`int` is 4 byte long which is 32 bit and the first bit(leftmost) **Most Significant Bit (MSB)** if not `unsigned`

actual value it can hold is

```text
2 ^ (16 - 1)
```

**MSB** 0 means non-negative which includes 0
1 means negative value

### Unsigned

means for int it uses all 16 bits to

```c
unsigned int a;
```

---

### Float and Double

---

### Modifier

```c
short int a
long int b
long long int c

// you can omit int
short x
long y
long long z

unsigned int d
unsigned long e

signed char f
unsigned char g
```
