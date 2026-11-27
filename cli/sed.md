# Sed

Parsing and transforming text.

## Reference

- [Man Page](https://man7.org/linux/man-pages/man1/sed.1.html)

---

| Uses                  | syntax                        |
| --------------------- | ----------------------------- |
| Substitution          | `sed 's/old/new' file.txt`    |
| In-place substitution | `sed -i 's/old/new' file.txt` |
| Delete line           | `sed '/pattern/d' file.txt`   |
| Print specific lines  | `sed -n 's/old/new' file.txt` |
