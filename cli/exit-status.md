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

```text
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

```text
127
```

- Means command `foobar` was not found.
