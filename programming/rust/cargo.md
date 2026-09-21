# Cargo

How to use cargo with rust project.

## Table of Contents

- [Install](#install)
- [Create Project](#create-project)
- [Run](#run)
- [Build](#build)
- [Clean](#clean)
- [Check](#check)
- [Test](#test)
- [Format](#format)
- [Dependency](#dependency)
  - [Add Dependency](#add-dependency)
  - [Remove Dependency](#remove-dependency)
  - [Outdated Dependency](#outdated-dependency)
  - [Update Dependency](#update-dependency)
- [Update](#update)

---

## Install

Download from [rust-lang.org/install-rust](https://rust-lang.org/tools/install/) if using Windows.

Check installation:

```sh
rustc --version
cargo --version
```

---

## Create Project

```sh
cargo new <project-name>

# inside a existing directory
cargo init
```

---

## Run

Compile and run.

```sh
cargo run
```

---

## Build

```sh
cargo build

# more optimized
cargo build --release
```

Checkout [unemotioned/guessing-game.rs](https://github.com/unemotioned/guessing-game.rs#guessing-game) for `Compile vs Build`.

---

## Clean

Remove `target` directory and build artifacts.

```sh
cargo clean
```

---

## Check

Check project compile without error, faster than `cargo build`.

```sh
cargo check
```

---

## Test

Run all tests.

```sh
cargo test
```

---

## Format

Format using `rustfmt`.

```sh
cargo fmt

# check without editing file
cargo fmt --check
```

---

## Dependency

### Add Dependency

```sh
cargo add <dependency-name>
```

### Remove Dependency

```sh
cargo remove <dependency-name>
```

### Outdated Dependency

```sh
# install the tool
cargo install cargo-outdated

# use cargo-outdated
cargo outdated
```

### Update Dependency

```sh
# update outdated dependencies
cargo update

# specific dependency
cargo update -p <dependency-name>
```

---

## Update

Cargo/Rust toolchain itself.

```sh
rustup update
```
