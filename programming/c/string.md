# String

Difference between string as character array and pointer.

## Reference

[String In Char Array VS. Pointer To String Literal](https://youtu.be/Qp3WatLL_Hc)

## Table of Contents

- [Declare](#declare)
- [Modify](#modify)
- [Assign](#assign)
- [Increment](#increment)
- [Sizeof](#sizeof)

---

## Declare

```c
char x[] = "this is array";

char *y = "this is pointer";
```

- `char arr`: copy of string literal including `\0`
- `char pointer`: addr of a string literal nul char is stored at the end of the
  string literal

---

## Modify

```c
x[0] = 'O';
printf("%s\n", x); // Ohis is array

y[0] = 'P';
printf("%s\n", y); // Undefined Behavior
```

- `Undefined Behavior`: might cause **segmentation fault** or seems to work
  normally

```c
const char *z = "this is const pointer";

z[0] = 'X'; // ERROR
```

- use `const` keyword to not modify string literal it points to

---

## Assign

```c
x = "Reassigning to char array"; // ERROR

y = "Reassigning to char pointer";
```

- `char arr`: **Array type 'char[n]' is not assignable**
- `char pointer`: pointer to point to another string literal

```c
#include <string.h>

// ...

strcpy(x, "Reassigned to char array."); // VALID
```

- if the length of strings are the same

---

## Increment

```c
x++; // ERROR

y++;
printf("%s\n", y); // his is pointer
```

- `char arr`: **Cannot increment value of type 'char[14]'**
- `char pointer`: pointer to points to next char

---

## Sizeof

```c
printf("x: %zu\n", sizeof(x));

printf("y: %zu\n", sizeof(y));
```

- `char arr`: return char count in array. including **NUL** char
- `char pointer`: return pointer type size

```c
printf("terminator: %d\n", x[sizeof(x) - 1]);
```

- `NUL(terminator)`: is `0` in byte.

```c
printf("x: %zu\n", strlen(x));

printf("y: %zu\n", strlen(y));
```

- use `strlen()` to get length or string literal char pointer is pointing to
- also works on char arr

> [!IMPORTANT]
> Dose not include **NUL** char even when used on char arr of string.

---

Check out [const pointer](./const-pointer.md) for more.
