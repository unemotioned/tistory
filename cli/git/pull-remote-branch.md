# Pull Remote Branch

When two branches have unrelated commit histories.

---

## List Remotes

- List only remotes:

```sh
git branch -r
```

- List local and remote:

```sh
git branch -a
```

## Create and Checkout

Create and checkout local branch tracking a remote branch:

```sh
git fetch origin # downloads remote changes without affecting locals
git checkout -b dev origin/dev # create `dev` branch which tracks `origin/dev` and checkout to `dev`
```
