# Typedef

Creating your own types.

## Reference

[how to start programming c - Magicalbat](https://www.youtube.com/watch?v=4-0GTazM5rY&t)

---

## Example

To have guaranteed size on different platforms.

```c
#include <stdint.h>
```

**Rust**, **Go** and **Zig** like type names.

```c
typedef int8_t i8;
typedef int16_t i16;
typedef int32_t i32;
typedef int64_t i64;

typedef uint8_t u8;
typedef uint16_t u16;
typedef uint32_t u32;
typedef uint64_t u64;

typedef i8 b8;   // 8-bit long boolean
typedef i32 b32; // 32-bit long boolean

typedef float f32;
typedef double f64;
```

```c
i32 x = 99;

printf("x: %d\n", x);
printf("sizeof x: %zu\n", sizeof(x)); // 4
```

---

- Tyepdef with [enum](./enum.md#typedef)
- Typedef with [struct](./struct.md#typedef)
