# Tistory

Notes while developing across machines.

| OS      | Window Manager                                        |
| ------- | ----------------------------------------------------- |
| macOS   | [Aerospace](https://github.com/nikitabobko/AeroSpace) |
| Arch    | [Hypr](https://hypr.land/)                            |
| Ubuntu  | [i3](https://i3wm.org/)                               |
| Windows | [GlazeWM](https://glazewm.com/)                       |

---

## Git

Good to know `git` commands.

### Merge

Update current branch without creating new merge commits, If possible.
For cleaner commit history.

```sh
git merge --ff-only {branch-name}
```

> `--ff-only`: --fast-forward-only

### Reset Commit History

Nuclear launch detected.

```sh
git checkout --orphan tmp # new branch with no commit history
git add -A
git commit -m "first commit"
git branch -D main        # remove main branch
git branch -m main        # rename current branch to main
git push -f origin main   # force push
```

### Pull Remote Branch

When two branches have unrelated commit histories.

```sh
git fetch origin               # downloads remotes changes without effecting locals
git checkout -b dev origin/dev # create `dev` branch which tracks `origin/dev` and checkout to `dev`
```

### Stop Tracking Ignored

After adding files to `.gitignore` which is already being tracked.

```sh
git rm -r --cached .
git add -A
git commit -m "Untrack ignored"
git push
```
