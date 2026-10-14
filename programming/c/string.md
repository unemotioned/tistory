# String

## Reference

[Beej's - Strings](https://beej.us/guide/bgc/html/split/strings.html#strings)

## Table of Contents

- [Declare](#declare)
- [Termination](#length)
- [Escape](#escape)
- [Length](#length)
- [Copy](#copy)

---

## Declare

since array is reference of first element and string is pointer to first character

```c
// as character array
char foo[] = "Foo";

// as pointer pointing to the first character of string
char *bar = "Bar";

char bar[] = "Bar"; // same as above
```

---

## Termination

`NUL` character or `\0`

> [!IMPORTANT]
> `NUL` is not a typo of null

in c string is saved as pointer to first char and nul char to indicate the end of string

```c
char *s = "foobar"; // actually "foobar\0"
```

---

## Escape

to store double quotes or other chars in string literal

```c
printf("He said \"I'm sober\".\n");
```

---

## Length

- `strlen()`: return string's char count in `size_t`

```c
#include <stdio.h>
#include <string.h> // include this

int main(void) {
  char s[] = "Hello, world!";

  int len = (int)strlen(s); // return in `size_t`

  printf("Length of s: %d\n", len);
}
```

---

## Copy

use `strcpy()` with `string.h` included

```c
char s[] = "Hello, world!";
char t[100];

char *u = s; // this will copy pointer of string

strcpy(t, s); // (destination, source)
```

now you can mutate t without effecting s
