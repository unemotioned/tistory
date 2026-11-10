# UTF-8 Character

Not every Korean characters are 3 bytes long.

## Table of Contents

- [Basic](#basic)
- [Wide Char](#wide-char)
- [Edit](#edit)
- [Troubleshooting](#troubleshooting)

---

## Basic

Using normal `char` type.

```c
#include <stdio.h>
#include <string.h>

int main() {
    char foo = '푸'; // Error
    const char *bar = "바";
    const char *kor = "동해물과 백두산이";

    printf("%s\n", bar);
    printf("%s\n", kor);

    printf("strlen bar_p: %zu\n", strlen(bar)); // 3 Byte
    printf("strlen kor_p: %zu\n", strlen(kor)); // 25 Byte (space as 1 Byte)

    return 0;
}
```

`char foo = '푸';`

```txt
Character too large for enclosing character literal type
```

---

## Wide Char

```c
#include <locale.h>
#include <stdio.h>
#include <wchar.h>

int main() {
    setlocale(LC_ALL, "");

    wchar_t wch = L'김';
    wchar_t wchars[] = L"동해물과 백두산이";

    printf("%lc\n", wch);
    printf("%ls\n", wchars);

    printf("size of wchar_t: %zu\n", sizeof(wchar_t));

    printf("wcslen of wchars: %zu\n", wcslen(wchars)); // 9

    return 0;
}
```

- `setlocale()`: Configure locale dependent behavior.
  - `(LC_ALL, "")`: Use system environment's locale.
  - `(LC_ALL, ".UTF-8")`: Apply all locale categories to `UTF-8` locale.

- `L` prefix makes the literal to `wchar_t`.

- `wchar_t`: 2 or 4 bytes depending on the platform

- `wcslen()`: length of **Wide Char String**, counts number of letters.

---

## Edit

Convert normal input of bytes into wide char string and edit them.

```c
#include <locale.h>
#include <stdio.h>
#include <stdlib.h>
#include <wchar.h>

int main() {
    setlocale(LC_ALL, "");

    char input[256];
    wchar_t chars[256];
    char output[512];

    printf("Enter: ");
    if (scanf("%255s", input) != 1) {
        return 1;
    }

    size_t len = mbstowcs(chars, input, sizeof(chars) / sizeof(chars[0]));

    // `mbstowcs()` returns (size_t)-1 on fail
    if (len == (size_t)-1) {
        return 1;
    }
    // converted wchar count is same as dest wchar arr size
    // no room for terminator
    if (len == 256) {
        return 1;
    }

    if (len > 0) {
        // change first char
        chars[0] = L'빵';
    }

    // `%ls` print specifier of wide char string
    printf("%ls\n", chars);

    // back to multi-byte string
    if (wcstombs(output, chars, sizeof(output)) == (size_t)-1) {
        return 1;
    }

    printf("Result: %s\n", output);

    return 0;
}
```

- `mbstowcs()`: From **Multi-byte String** to **Wide Char String**
  - Arguments: `dest`, `src`, `max number of wchars to write to` dest(which is
    wchar_t array)
  - Return:
    - **Success**: Number of wide chars converted
    - **Fail**: `(size_t)-1` which is same as `SIZE_MAX`

- `wcstombs()`: From **Wide Char String** to **Multi-byte String**
  - Arguments: `dest`, `src`, `max bytes to write` to write to dest
  - Return:
    - **Success**: Number of bytes written
    - **Fail**: `(size_t)-1`

> [!NOTE]
> If the buffer is too small `Null Terminator` might not be saved.

---

## Troubleshooting

Add following codes if UTF-8 characters are not displayed properly.

```c
#ifdef _WIN32
#include <windows.h>
#endif

int main() {
#ifdef _WIN32
    SetConsoleCP(CP_UTF8);       // input
    SetConsoleOutputCP(CP_UTF8); // output
    setlocale(LC_ALL, ".UTF-8");
#endif
    setlocale(LC_ALL, "");

    printf("%s\n", "창문을 여세요");

    return 0;
}
```

More about [Macro Condition](./macro-condition.md).
