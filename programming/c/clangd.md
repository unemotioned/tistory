# Clangd

Configuration to diagnose same as from compile-time while inside an editor.

---

Inside `.clangd`:

```yaml
CompileFlags:
  Add:
    - -xc
    - -std=c11
    - -Wall
    - -Wextra
    - -pedantic
```

- `-xc`: Parse files as `c`.

> [!TIP]
> `-xc++` for **C++**.

---

Check out [gcc.md](./gcc.md) for more about compile flags.
