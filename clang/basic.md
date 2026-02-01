# C Basic

## Basic Structure

### Required Header

```c
#include <stdio.h>
```

Header file for printing to terminal.

### Main Function

```c
int main() {
    return 0;
}
```

- Returns `0` on success
- Any other value indicates failure

### Statement Syntax

```c
printf("Hello, World!");
```

Semicolon (`;`) required to end statements.

---

## Compiler vs Interpreter

### Compiler

- Converts entire codebase into machine code or executable
- Catches errors at compile time
- Runs faster than interpreted languages
- Produces executable files

### Interpreter

- Reads and executes code line by line
- Runs until it encounters an error
- No executable output files

---

## Comments

```c
// Single-line comment

/*
   Multi-line
   comment
*/
```

---

## Data Types

**Note:** 1 byte = 8 bits

| Type     | Size    | Description                     |
| -------- | ------- | ------------------------------- |
| `int`    | 4 bytes | Integer values                  |
| `float`  | 4 bytes | Floating-point numbers          |
| `double` | 8 bytes | Double-precision floating-point |
| `char`   | 1 byte  | Single character                |
| `char *` | Varies  | Array of characters (string)    |

**Important:** Type casting is not allowed implicitly.

### Strings

In C, strings are arrays of characters.

```c
char *msg_from_dax = "You still have 0 users";
```

- Use double quotes (`"`) for strings
- Use single quotes (`'`) for single characters

### Function Returning String

```c
char *get_temperature_status(int temp);
```

---

## Printing Variables

### Format Specifiers

| Specifier | Type              |
| --------- | ----------------- |
| `%d`      | Integer (decimal) |
| `%f`      | Float             |
| `%c`      | Character         |
| `%s`      | String (char \*)  |
| `%zu`     | size_t            |

### Examples

```c
printf("Default max threads: %d\n", sneklang_default_max_threads);
printf("Custom perms: %c\n", sneklang_default_perms);
printf("Constant pi value: %f\n", sneklang_default_pi);
printf("SnekLang title: %s\n", sneklang_title);
```

---

## Constants

Variables whose values cannot be changed.

```c
const int pi = 3.14;
```

---

## Functions

### Void as Parameter

Explicitly accepts no arguments.

```c
int noArgs(void) {
    return 37;
}
```

### Void as Return Type

Returns nothing.

```c
void noReturn() {
    printf("foobar");
}
```

---

## Header Files

Header files (`.h`) contain function prototypes without implementation.

```c
// explain.h
float get_average(int x, int y, int z);
```

Components:

- Return type
- Function name
- Parameters
- No implementation logic

---

## Division & Type Casting

### Division Rules

- Integer division: `int / int` discards remainder
- Float division: `float / float` preserves decimal

### Example with Mixed Types

```c
float get_average(int x, int y, int z) {
    float total = x + y + z;
    return total / 3;
}
```

### Type Casting

```c
int x = 5;
float y = (float)x;
```

---

## Mathematical Operations

```c
x++   // Post-increment
y--   // Post-decrement
++z   // Pre-increment
--w   // Pre-decrement
```

---

## Logical Operators

**Precedence (highest to lowest):**

1. `!` (NOT)
2. `&&` (AND)
3. `||` (OR)

---

## Ternary Operator

Compact conditional expression that returns a value.

```c
int max = a > b ? a : b;
```

**Syntax:** `condition ? value_if_true : value_if_false`

**Note:** While concise, if statements are often more readable.

---

## sizeof Operator

Returns the size of a variable or type in bytes.

```c
printf("sizeof(char) = %zu\n", sizeof(char));
printf("sizeof(size_t) = %zu\n", sizeof(size_t));
```

**Note:** `size_t` represents the largest possible object size on the target platform.

---

## Control Flow

### For Loop

```c
for (initialization; condition; final_expression) {
    // Loop body
}
```

### While Loop

```c
while (condition) {
    // Loop body
    // Include increment/decrement to avoid infinite loop
}
```

### Do-While Loop

Executes loop body at least once before checking condition.

```c
do {
    // Loop body
} while (condition);
```

**Note:** Semicolon required after `while` statement.

---

## Header File Protection

### Pragma Once

Ensures header file is included only once, regardless of how many times it's referenced.

```c
// foo.h
#pragma once

struct Point {
    int x;
    int y;
};
```

### Header Guards

Traditional method using preprocessor directives.

```c
#ifndef FOO_H
#define FOO_H

// Header content

#endif
```

**Purpose:** Prevents redefinition errors when header files are included multiple times.
