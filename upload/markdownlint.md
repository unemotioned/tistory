# Markdown Lint

how to disable line length linting

## Line Length

in `.markdownlint.json` or `.markdownlint.jsonc`

```jsonc
{
  "MD013": false,
}
```

```jsonc
{
  "MD013": { "line_length": 200 },
}
```

## Prettier

in `.prettierrc`

```jsonc
{
  "proseWrap": "never", // "always" | "never" | "preserve"
}
```

- `always`: wrap exceeding line
- `never`: paragraph into single line
- `preserve`: no tempering
