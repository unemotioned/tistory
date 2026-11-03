# [Biome](https://biomejs.dev/)

Faster linting and formatting tool chain.

## Table of Contents

- [Install](#install)
- [Init](#init)
- [Commands](#commands)
- [Config](#config)

---

## Install

### Globally

```sh
npm i -g @biomejs/biome
```

### As Dependency

- `-D`: `--save-dev` - exclude from production
- `-E`: `--save-exact` - exact version instead of a range

```sh
npm i -D -E @biomejs/biome
```

---

## Init

Creates a `biome.json` file with defaults at the project root.

```sh
npx @biomejs/biome init
```

> [!TIP]
> File name is also available in `JSONC` and can be prefixed with dot.

---

## Commands

```sh
# format
npx biome format --write .

# lint and apply safe fix
npx biome lint --write .

# format, organize imports and lint
npx biome check --write .
```

---

## Config

[Biome Configuration](https://biomejs.dev/reference/configuration/)

**My style**:

- Indent Style: `Space`
- Indent Width: `4`
- Line Width: `100`
- Line Ending: `LF`
- Quote Style: `Single`
- Trailing Comma: `All`

Inside `.biome.jsonc`:

```jsonc
{
  "$schema": "https://biomejs.dev/schemas/2.6.4/schema.json",
  "formatter": {
    "indentStyle": "space",
    "lineEnding": "lf",
  },
  "javascript": {
    "formatter": {
      "indentWidth": 4,
      "lineWidth": 100,
      "quoteStyle": "single",
      "trailingCommas": "all",
    },
  },
  "json": {
    "formatter": {
      "trailingCommas": "all",
    },
  },
}
```

> [!NOTE]
> `javascript` in biome includes **JSX**, **TS** and **TSX**.

---

<!-- TODO: finish documenting migration -->

## Migration

### Prettier

### Eslint

---

<!-- TODO: finish documenting github action -->

## GitHub Action
