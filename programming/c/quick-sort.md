# Quick Sort

How to write compare function for `qsort()`.

```c
#include <stdlib.h>
```

---

## Call QSort

```c
int compare(const void *a, const void *b);

int main() {
    int nums[] = {-1, 0, 1, 2, -1, -4};
    qsort(nums, sizeof(nums) / sizeof(nums[0]), sizeof(nums[0]), compare);

    return 0;
}
```

- `Base`: Array to sort.
- `NumOfElements`: Number of elements in the base array.
- `SizeOfElements`: Data type size of elements.
- `CompareFunction`: How to compare each elements which return int type.

---

## Compare Function

```c
int compare(const void *a, const void *b) {
    int x = *(const int *)a;
    int y = *(const int *)b;

    return (x > y) - (x < y);
}
```

- `const void *a`: const generic pointer to not mutate the value from this function.
- `*(const int *)a`: cast pointer type to int and dereference it.
- `return`:
  - x is larger: (1) - (0) -> 1 == x should come **after** y
  - x is smaller: (0) - (1) -> -1 == x should come **before** y
  - equal: (0) - (0) -> 0

> [!TIP]
> Change the return expression to `(x < y) - (x > y)` to sort in descending order.
