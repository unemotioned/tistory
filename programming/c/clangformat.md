# [ClangFormat](https://clang.llvm.org/docs/ClangFormatStyleOptions.html)

Formatter for C and C++.

**My Style**:

- Indent Style: `Space`
- Indent Width: `4`
- Column Limit: `100`
- Opening Brace: `Same Line`
- Pointer Alignment: `Right`

---

## Config

Inside `.clang-format`:

```yaml
---
BasedOnStyle: LLVM
UseTab: Never
IndentWidth: 4
ColumnLimit: 100

AllowShortFunctionsOnASingleLine: None

BreakAfterAttributes: Always
BreakBeforeBraces: Attach # opening brace always on same line

# args and params into one per line if it does not fit
PackArguments:
  BinPack: OnePerLine
PackParameters:
  BinPack: OnePerLine

PointerAlignment: Right
```

---

## Commands

Format file and write directly:

- `-i` (in-place)

```sh
clang-format -i *.c
```

Format using nearest `.clang-format` file:

```sh
clang-format -i --style=file *.cpp
```

### Recursively

**Fd**:

```sh
find . -type f \( -name "*.cpp" -o -name "*.h" -o -name "*.hpp" \) -exec clang-format -i --style=file {} +
```

- `find .`: recursively search from current dir
- `-type f`: only matches files
- `-name`: match by file extensions
- `-o`: logical **OR**
- `{} +`: process multiple files per invocation for efficiency
