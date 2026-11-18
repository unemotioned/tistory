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
    - -Wpedantic
```

- `-xc`: Parse files as `c`.

> [!TIP]
> `-xc++` and `-std=c++14` for **CPP**.

---

Check out [gcc.md](./gcc.md) for more about compile flags.
