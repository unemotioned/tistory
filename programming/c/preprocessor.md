# Preprocessor

---

## Conditionals

- `__APPLE__`
- `__linux__`
- `_WIN32`
- `_WIN64`

### ifdef

```c
#ifdef _WIN32
#include <windows.h>
#endif
```

---

### ifndef

```c
#ifndef __APPLE__
// if not macOS or iOS
#endif
```

---

### elif

```c
#if defined(__APPLE__) || defined(__linux__)
    unix_func();
#elif defined(_WIN32) && defined(_WIN64)
    win_func();
#endif
```

### if not

```c
#if !defined(_WIN32) && !defined(_WIN64)
// just don't use Windows
#endif
```
