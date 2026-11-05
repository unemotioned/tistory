# Ignore

Different ways to ignore directories.

---

## Itself and Everything

Cannot re-include file or directory under it.

```gitignore
.vscode/
```

---

## Directly Under

Can re-include file and directory under it.

```gitignore
.idea/*
!.idea/dictionaries/project.xml
```

---

## Recursively

Can re-include file under it but not directory.

```gitignore
.vscode/**
!.vscode/settings.json
```
