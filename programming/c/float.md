# Float in Binary

C stores floating-point numbers using the [IEEE 754](https://en.wikipedia.org/wiki/IEEE_754) standard.

## Reference

[Geeks For Geeks - C Float and Double](https://www.geeksforgeeks.org/c/c-float-and-double/)

## Table of Contents

- [The Equation](#the-equation)
- [Float Type](#float-type)
- [Double Type](#double-type)
- [Decimal to Binary](#decimal-to-binary)
  - [Fraction to Binary](#fraction-to-binary)
  - [1. Sign](#1-sign)
  - [2. Mantissa](#2-mantissa)
  - [3. Exponent](#3-exponent)
  - [Result](#result)

---

## The Equation

Float and double types in memory is separated into parts of **Sign**, **Fraction** and **Exponent**.

```math
(-1)^S \times M \times 2^E
```

- `Sign`: 부호
- `Mantissa`: 가수
  - `Fraction`: 소수부
  - `Significand`: 유효숫자부
- `Exponent`: 지수

---

## Float Type

```c
float f = 3.14f;  // suffix `f`

// %f
scanf("%f", &f);
printf("%f", f); // when printing float automatically gets promoted to double
```

4 Bytes / 32 Bits

Sign: 1 bit
Exponent: 8 bits
Fraction: 23 bits

```txt
31             30              23 22                 0
+-------------+------------------+-------------------+
| sign: 1 bit | exponent: 8 bits | fraction: 23 bits |
+-------------+------------------+-------------------+
```

---

## Double Type

```c
double d = 3.14;

// %lf
scanf("%lf", &d);
printf("%f", d); // used %f specifier even when printing double
```

8 Bytes / 64 Bits

- Sign: 1 bit
- Exponent: 11 bits
- Fraction: 52 bits

```txt
63             62               52 51                 0
+-------------+-------------------+-------------------+
| sign: 1 bit | exponent: 11 bits | fraction: 52 bits |
+-------------+-------------------+-------------------+
```

---

## Decimal to Binary

```txt
65.125
65    (10) = 1000001 (2)
0.125 (10) = 0.001   (2)

65.125 (10) = 1000001.001       (2)
            = 1.000001001 * 2^6 (2)  // normalization(정규화)
```

### Fraction to Binary

In Decimal fraction is `1/10`, `1/10^2`, `1/10^3`, ... so on. Same stuff for the
binary:

```txt
0 . 1   2   5
    |   |   |
   1/2 1/4 1/8
```

To convert it to binary, we multiply it and check the integer part:

```txt
0.125 * 2 = 0.250
Integer part: 0 -> Binary digit: 0

0.250 * 2 = 0.500 -> 0
0.500 * 2 = 1.000 -> 1

Fraction part is all 0. We're done.
==> 001
```

### 1. Sign

- **-1** powered by `0` = **1** ==> `Positive`
- **-1** powered by `1` = **-1** ==> `Negative`

Sign: `0`

### 2. Mantissa

Or fraction.

After normalization leftmost bit will always be 1. So **IEEE 754** will not store
it and just save the last 9 bits.

Left over 14 bits will be filled with 0s.

Fraction: `00000100100000000000000`

### 3. Exponent

```math
Exponent = Bias + Real Exponent
```

- **Real Exponent**: The number you get after normalization.
- **Bias**: Exponent can be a negative number so we use bias to store them

```math
Bias = 2^{k-1}-1
```

Exponent bit size in float is **8**. And after normalization we got **6**.

```txt

2 ^ (8 - 1) -1 = 127

127 + 6 = 133

133 (10) = 10000101 (2)
```

Exponent: `10000101`

> [!IMPORTANT]
> The exponent from binary to decimal equation actually uses **Real Exponent**
> which is `Exponent - Bias`.

### Result

`65.125` in raw bits as **float type**:

```txt
0              10000101           00000100100000000000000

31             30              23 22                    0
+-------------+------------------+----------------------+
| sign: 1 bit | exponent: 8 bits | fraction: 23 bits    |
+-------------+------------------+----------------------+
```

Result: `01000010100000100100000000000000`
