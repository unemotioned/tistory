# Clangd

LSP to read files as **C** language.

- Warning:

```txt
Invalid argument '-std=c11' not allowed with 'Objective-C++'
```

Inside `.clangd`:

- `-xc`: parse files as `c`

```yaml
CompileFlags:
  Add: [-xc, -std=c11]
```

> [!TIP]
> `-xc++` for **C++**.
