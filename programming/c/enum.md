# Enum

Represent fixed set of integer constants using meaningful names.

## Table of Content

- [Basic](#basic)
- [Typedef](#typedef)
- [Switch Case](#switch-case)
- [Manually Setting Values](#manually-setting-values)

---

## Basic

```c
enum Color {
    RED,   // 0
    GREEN, // 1
    BLUE,  // 2
};
```

- 1st element starts as value of 0
- Name of enum use **PascalCase**
- Name of elements use **SCREAMING_SNAKE_CASE**

```c
enum Color {
    RED,
    GREEN,
    BLUE,
} r = RED,
  g = GREEN;
```

- Declaring variable directly after enum definition.

> [!TIP]
> Optional comma after last element keeps the formatter from collapsing the
> short enum declaration.

```c
int main(void){
    enum Color color = getColor();

    switch (color)
    case RED:
        printf("RED\n");
    break;

    return 0;
}
```

---

## Typedef

- Declare anonymous enum and then give it a alias.
- Later you can reference it without `enum` keyword.

```c
typedef enum {
    RED,
    GREEN,
    BLUE,
} Color;

int main(void) {
    Color r = RED;
}
```

---

## Switch Case

`clangd` will warn unhandled enum values.

```c
switch (color) {
case RED:
    printf("The color is red\n");
    break;
case GREEN:
case BLUE:
    printf("The color is NOT red\n");
    break;
}
```

> [!TIP]
> No `default` case can help when new enum values are added.

---

## Manually Setting Values

```c
typedef enum {
    A,    //  0: default starting value
    B,
    C=4,  //  4: manually set
    D,    //  5: continue in positive direction
    E,
    F=4,  //  4: duplication is ok
    G=-1, // -1: even negative numbers
} Alphabet;

int main(void) {
    Alphabet charlie = C;

    printf("%d\n" charlie == F); // 1 (true)
}
```

- Duplicated values are indistinguishable at runtime.

```c
Alphabet alpha = get_alpha();

switch (alpha) {
    case C:
        printf("C\n");
    break;
    case F:
        printf("F\n");
    break;
}
```

- Duplicated values are not allowed as separate case under single switch.
