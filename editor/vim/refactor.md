# Refactor

Refactoring without plugins.

## Reference

[3 Levels of Vim Refactoring - typecraft](https://www.youtube.com/watch?v=oQB8lYUZtrY)

---

## 1. Find RegEx from File Types

```sh
:vimgrep /kr.or.iei/ `find . -type f`
```

## 2. Open Quick-fix List

```sh
:copen
```

## 3. Edit Quick-fix List with Substitute

```sh
:cdo %s/kr.or.iei/com.unemotioned/gc
```

- `cdo`: inside QFlist
- `%s/.../.../`: substitute that into this
- `gc`: **globally** (every occurrence on same line), **confirmation** (requires
  consent)
