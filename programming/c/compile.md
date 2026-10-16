# Compile

## Command

[gcc(1) - Linux manual page](https://man7.org/linux/man-pages/man1/gcc.1.html)

```sh
gcc -std=c23 -Wall -Wextra -pedantic -O2 main.c -o a
```

- `-std=`: determines the language standard
  - `c99`: no need to `return 0;` at then end of main
  - `c11`: portable and modern enough without being too new
  - `c23`: `void` and empty params behaves exactly the same
- `-Wall`: warnings that some users consider questionable, and that are easy to avoid
- `-Wextra`: extra warnings that are not enabled by -Wall
- `-pedantic`: all warnings demanded by strict ISO C standard
- `-O2`: standard optimization
  - `-O0`: no optimization
  - `-O1`: basic optimization
  - `-O3`: aggressive optimization
- `main.c`: file name to compile
- `-o a`: place output file at file `a`

> [!NOTE]
> Same flags work exactly the same with `clang`.

---

## Clangd

### Troubleshooting

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
