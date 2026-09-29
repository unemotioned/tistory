# Input

getting input from user via terminal

```rust
use std::io::{self, Write};
```

## Table of Contents

- [String](#string)
- [Integer](#integer)

---

## String

```rust
fn get_user_input() {
  let mut input = String::new();

  println!("Say something");
  print!("=> ");

  io::stdout().flush().unwrap();

  io::stdin()
    .read_line(&mut input)
    .expect("Failed to read line");

  let str: &str = input.trim();

  println!("{str}");
}
```

- `mut` keyword is necessary when taking input
- `io::stdout().flush().unwrap()` flush stdout to prompt `print!()` immediately
- `unwrap()` to panic on fail, can be replaced with `expect("Failed to flush stdout")`
- `&mut input` mutable reference to input variable to borrow and edit without owning it
- `trim()` return `&str` slice without leading and trailing whitespaces

```rust
// into owned string
let foo: String = input.trim().to_string();
```

---

## Integer

```rust
fn get_int() {
  let mut input = String::new();

  println!("Enter a number");

  io::stdin()
    .read_line(&mut input)
    .expect("Failed to read line");

  let n: i32 = input.trim().parse().expect("Enter a integer type");
}
```

### Multiple Integers

```rust
fn get_multi_ints() {
  let mut input = String::new();

  println!("Enter numbers");

  io::stdin()
    .read_line(&mut input)
    .expect("Failed to read line");

  let nums: Vec<i32> = input
    .trim()
    .split_whitespace()
    .map(|x| x.parse().unwrap())
    .collect();
}
```
