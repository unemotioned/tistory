# Vector

If number of elements is fixed at compiled time then consider using array.

## Table of Contents

- [Initialize](#initialize)
- [Append](#append)
- [Access](#access)
- [Iterate](#iterate)
- [Array to Vec](#array-to-vec)

---

## Initialize

```rust
let mut v: Vec<i32> = Vec::new();

// declare with size
let mut v1: Vec<i32> = Vec::with_capacity(3);

// declare and initialize
let v2 = vec![1, 2, 3];
```

`vec![]` macro is better than declaring and then appending.

---

## Append

```rust
v.push(0);
```

---

## Access

```rust
let third = &v[20];
```

> [!WARNING]
> Panic at **runtime** if index is out of bounds.

This won't.

```rust
match v.get(20) {
    Some(e) => println!("21th element: {}", e),
    None => println!("There is no 21th element")
}
```

---

## Iterate

```rust
for i in &v {
    println!("{}", i);
}

// iterate and mutate
for i in &mut v {
    // dereference
    *i += 50;
}
```

- `i`: mutable reference to element
- `*i`: access actual element to change it

---

## Array to Vec

```rust
let arr = [1, 2, 3];

let v = arr.to_vec();
// or
let v = Vec::from(arr);
```

- **to_vec()**: clone each element into new Vec (which can be expensive)
- **Vec::from()**: transfer ownership (move)
