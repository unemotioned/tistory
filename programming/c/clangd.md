# Clangd

LSP to read files as **C** language.

---

## Troubleshooting

**Warning**: LSP is treating header file as Objective-C++

```txt
Invalid argument '-std=c11' not allowed with 'Objective-C++'
```

Inside `.clangd`:

- `-x`: parse files as `c`

```yaml
CompileFlags:
  Add: [-xc, -std=c11]
```

> [!TIP]
> `-xc++` for **C++**.
