# Fuzzy Find

Built in fuzzy find.

## Reference

- [You Might Not Need a Fuzzy Finder - Marco Peluso](https://www.youtube.com/watch?v=eXo7Yo0Uc-w)

---

## Find

Open help document:

```vim
:h find<CR>
```

Fuzzy search file:

```vim
:fin **/foo.md<CR>
```

- `<Tab>` completion is available.

Add downward path:

```vim
:set path+=**
```

> [!NOTE]
> Read `:h starstar` for more.

Open in hor/vert split:

```vim
" open in horizontal split
:sfin bar.md<CR>

" open in vertical split
:vertical sfin baz.md<CR>
```

> [!TIP]
> Alias `vert` is also allowed.
