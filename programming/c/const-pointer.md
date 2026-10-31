# Constant and Pointer

<!-- Changing constants is the only constant I know of that can change constantly. -->

_If you change how constantly the constants change constantly then why change anything?_

_Because it changes everything._

<p align="center">
  <img src="../../assets/constant-zach.png" alt="constant-zach.png" width="512px"/>
</p>

> [The day that addition was invented](https://www.youtube.com/watch?v=SYHEdko6RcI)
> Zach Start Himeslef

---

## Reference

[Constant Pointer VS. Pointer To A Constant](https://www.youtube.com/watch?v=egvGq3WSF9Y)

## Table of Contents

- [Const Pointer](#const-pointer)
- [Pointer to Const](#pointer-to-const)
- [Const Pointer to Const](#const-pointer-to-const)
  - [Correct Way](#correct-way)
- [Summary](#summary)

---

## Const Pointer

pointer is constant

- cannot change it to point to something else
- allowed to change dereferenced value

```c
char a = 'a';
char b = 'b';

char *const a_p1 = &a;

a_p1 = &b; // Error

*a_p1 = 'c'; // Valid
```

---

## Pointer to Const

cannot change value via the pointer

- allowed to change what it points to
- cannot change dereferenced value

```c
char const *a_p2 = &a;
const char *a_p3 = &a; // same type

a_p2 = &b; // Valid

*a_p2 = 'c'; // Error
```

> [!NOTE]
> Actual object can be modified through other reference.

---

## Const Pointer to Const

pointer to const must honor its const-ness

```c
const char x = 'x';
const char y = 'y';
const char z = 'z';

char *x_p = &x; // Warn
x_p = &y;       // Warn
*x_p = 'z';     // Undefined Behavior

const char *y_p = &y;
y_p = &z; // Valid
*y_p = z; // Error
```

- `*x_p = 'z'`: Undefined Behavior
- `y_p`: this is **pointer to const**
  - still can point to other address
  - but not allowed to change dereferenced value

### Correct Way

```c
const char *const z_p = &z;
char const *const z_p2 = &z; // same type

z_p = &x; // Error
*z_p = y; // Error
```

- pointer cannot be changed to another address
- dereferenced value cannot change

---

## Summary

| Type                         | Value     | Pointer   |
| ---------------------------- | --------- | --------- |
| `Const Pointer to Non-Const` | Mutable   | Imutable  |
| `Pointer to Const`           | Immutable | Mutable   |
| `Const Pointer to Const`     | Immutable | Immutable |
