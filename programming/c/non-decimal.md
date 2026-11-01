# Non-Decimal

How to assign integer type with binary, octal and hexadecimal literals.

## Table of Contents

- [Binary](#binary)
- [Octal](#octal)
- [Hexadecimal](#hexadecimal)
- [How to Count](#how-to-count)
- [How to Convert](#how-to-convert)

---

## Binary

`0b` or `0B` prefix

```c
int bin = 0b1010; // 10 (2)
```

---

## Octal

`0` prefix

```c
int oct = 012; // 10 (8)
```

---

## Hexadecimal

`0x` or `0X` prefix

```c
int hex = 0xA; // 10 (16)
```

---

## How to Count

| Decimal | Octal | Hexadecimal |
| ------- | ----- | ----------- |
| 0       | 0     | 0           |
| 1       | 1     | 1           |
| 2       | 2     | 2           |
| 3       | 3     | 3           |
| 4       | 4     | 4           |
| 5       | 5     | 5           |
| 6       | 6     | 6           |
| 7       | 7     | 7           |
| 8       | 10    | 8           |
| 9       | 11    | 9           |
| 10      | 12    | A           |
| 11      | 13    | B           |
| 12      | 14    | C           |
| 13      | 15    | D           |
| 14      | 16    | E           |
| 15      | 17    | F           |
| 16      | 20    | 10          |

`31` (10) == `1F` (16) == `20` (8)

---

## How to Convert

<!-- TODO: doc how to convert from dec to others -->

---

How to print in **Binary**, **Octal** or **Hexadecimal**: [printf.md](./printf.md#non-decimal)
