# GitHub CLI

## Table of Contents

- [Install](#install)
- [Authenticate](#authenticate)
- [Clone](#clone)
- [Create Repository](#create-repository)

---

## Install

From AUR repository with yay:

```sh
yay -S github-cli
```

Check install:

```sh
gh --version
```

---

## Authenticate

```sh
gh auth login
```

---

## Clone

```sh
gh repo clone <owner>/<repo>
```

From your repository

```sh
gh repo clone <repo>
```

---

## Create Repository

Initialize and create at least commit first

From existing local git repo:

```sh
gh repo create <repo-name> --source=. --public --push
```

Flags:

- `--source=.` - current directory
- `--private` or `--public` - visibility
- `--push` - push local code immediately

For more:

```sh
gh repo create -h
```
