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

This one won't:

```rust
match v.get(20) {
    Some(e) => println!("21st element: {}", e),
    None => println!("There is no 21st element")
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

let v1 = arr.to_vec(); // Clone

// or
let v2 = Vec::from(arr); // Move
```

- `to_vec()`: Clones each element into new `Vec`, which can be expensive.
  Original array is still available.

- `Vec::from()`: Move elements into new `Vec`, transferring ownership. Original
  array becomes unavailable.

> [!IMPORTANT]
> `i32` data type has **Copy Trait**. Array containing non-copy types becomes
> unavailable.
