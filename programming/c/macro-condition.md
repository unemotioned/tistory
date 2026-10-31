# Macro Condition

`Conditional Compilation Directives`: Preprocessor to include or exclude codes
before compilation.

---

## Conditionals

- OSs and architecture
  - `__APPLE__`: macOS or iOS
  - `__linux__`
  - `_WIN32`: 32 or 64 bit
  - `_WIN64`

### ifdef

```c
#ifdef _WIN32
#include <windows.h>
#endif
```

### ifndef

same as `#if !defined(NAME)`

```c
#ifndef __APPLE__
// if not macOS or iOS
#endif
```

### elif

```c
#if defined(__APPLE__) || defined(__linux__)
    unix_func();
#elif defined(_WIN32)
    win_func();
#endif
```

### if not

```c
#if !defined(_WIN32)
    unix_func();
#endif
```
