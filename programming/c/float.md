# Float to Binary

convert floating point number from decimal to binary

## Reference

[Geeks For Geeks - C Float and Double](https://www.geeksforgeeks.org/c/c-float-and-double/)

Binary fraction into decimal:

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
printf("%f", f);
```

4 Bytes / 32 Bits

Sign: 1 bits
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
printf("%lf", d); // printf will round the 7th digit
```

8 Bytes / 64 Bits

- Sign: 1 bits
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
65 = 1000001
0.125 = 001

65.125 = 1000001.001
       = 1.000001001 * 10^6 // normalization(정규화)
```

### 1. Sign

**-1** powered by `0` == **1** == `positive`
**-1** powered by `1` == **-1** == `negative`

### 2. Mantissa

`1000001001` is 10 bits long

but since after normalization leftmost bit will always be 1
so c will omit it and just save the last 9 bits

left over 14 bits will be filled with 0s

### 3. Exponent

since exponent can be negative number use `bias` to store them

exponent bit size in float type is 8

10000000 (2) = 127 (10) and 127 is called `bias`

127 + 6 = 133

finally 133 (10) == 10000101 (2) will be stored

```math
Real Exponent = Exponent - Bias
```

> [!NOTE]
> The size of `Bias` varies by type.

```txt
65.125 in raw bits

0              10000101           00000100100000000000000

31             30              23 22                    0
+-------------+------------------+----------------------+
| sign: 1 bit | exponent: 8 bits | fraction: 23 bits    |
+-------------+------------------+----------------------+
```
