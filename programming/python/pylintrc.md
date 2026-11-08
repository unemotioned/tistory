# Pylintrc

Python linter remote control

---

## Suppress Warnings

Inside `.pylintrc`:

```dosini
[MESSAGES CONTROL]
disable =
    missing-docstring,
    too-few-public-methods,
    wrong-import-order,
```

- `missing-docstring` includes:
  - `missing-module-docstring`
  - `missing-class-docstring`
  - `missing-function-docstring`
