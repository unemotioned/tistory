# CPU Cache Line

Cache Line:

- Smallest unit of data transfer between RAM and CPU cache.
- 64 bytes on modern x86 machines.

Order member of struct from large data types to small to minimize padding when
CPU reads from RAM.

## Reference

[C Struct Alignment and Padding](https://www.w3schools.com/c/c_structs_padding.php)

---

## Data Layout Optimization

**Struct Padding**:

C compiler may add some padding between members to align data in memory
properly. Which makes the CPU to read it more efficiently. Eventually making the
program to run faster.

```c
typedef struct {
    char a;   // 1
    char b;   // 1
    double c; // 8
    int d;    // 4
    //   Total: 14
} Bad;

// ...

printf("sizeof Bad : %zu\n", sizeof(Bad)); // 24 (192 bits)
```

- Padding: 10 Bytes

Same members but reordered:

```c
typedef struct {
    double c;
    int d;
    char a;
    char b;
} Good;

// ...

printf("sizeof Good: %zu\n", sizeof(Good)); // 16
```

- Padding: 2 Bytes
