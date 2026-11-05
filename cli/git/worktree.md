# Worktree

When you have uncommitted changes but have to work on something else.

## Table of Contents

- [List](#list)
- [Create](#create)
- [Remote](#remove)
- [Prune](#prune)

---

## List

```sh
git worktree list
```

---

## Create

Create `foo` project that have `feature/bar` branch checked out.

```sh
git worktree add ../foo -b feature/bar

git worktree add ../foo feature/bazz # use existing branch (must be different branch from current one)

git worktree add ../foo # new worktree that create and checkout branch foo
```

1. Open the worktree as separate project.
2. Edit and commit normally from new worktree.

---

## Remove

```sh
git worktree remove ../foo

git branch -d feature/bar # remove merged

git branch -D feature/bar # or remove unmerged
```

---

## Prune

Clean up stale worktree metadata.

```sh
git worktree prune
```
