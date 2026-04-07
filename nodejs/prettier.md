# Prettier

[prettier.io](https://prettier.io/)

HTML, CSS, JavaScripts, Markdown, JSON etc formatter

## Table of Contents

- [Prettierrc](#prettierrc)
- [Configuration](#configuration)

---

## Prettierrc

create `.prettierrc` file at project root directory

minimal useful configs:

```jsonc
{
  "tabWidth": 4, // default: 2
  "singleQuote": true, // default: false
}
```

## Configuration

[Overrides](https://prettier.io/docs/configuration#configuration-overrides)

just for javascript files

```jsonc
{
  "overrides": [
    {
      "files": ["*.js", "*.mjs"],
      "options": {
        "tabWidth": 4,
        "singleQuote": true,
      },
    },
  ],
}
```
