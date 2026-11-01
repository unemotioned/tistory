# Exit Status

Exit status of most recent command.

---

`$?`

```sh
echo $?
```

---

**Example**:

```sh
gcc main.c -o main && ./main
echo $?
```

**Result**:

```txt
0
```

- `0`: successful
- `Non-Zero`: not successful

> [!IMPORTANT]
> Check it immediately after running command.

---

From the terminal:

```sh
foobar

echo $?
```

**Result**:

```txt
127
```

- Means command `foobar` was not found.
