# Tistory

How to setup my machines.

| OS      | Window Manager                                        |
| ------- | ----------------------------------------------------- |
| macOS   | [Aerospace](https://github.com/nikitabobko/AeroSpace) |
| Arch    | [Hypr](https://hypr.land/)                            |
| Ubuntu  | [i3](https://i3wm.org/)                               |
| Windows | [GlazeWM](https://glazewm.com/)                       |

## TODOs

- [ ] Create complete setup scripts
- [ ] Upload on [Tistory](https://unemotioned.tistory.com/)

---

## Git

create new branch

```sh
git branch {new-branch-name}
```

checkout the branch

```sh
git checkout {branch-name}
```

show workingtree differences

```sh
git diff
```

merge branch into current branch without creating new commit

`--ff-only`: fast-forward-only

```sh
git merge --ff-only {branch-name}
```

pull and push

`-u`: upstream

```sh
git pull
git push -u origin main
```

### Reset Commit History

```sh
git checkout --orphan tmp  # new branch with no commit history
git add -A
git commit -m "first commit"
git branch -D main       # remove main branch
git branch -m main       # rename current branch to main
git push -f origin main  # force push
```

### Pull Remote Branch

```sh
git fetch origin                # downloads remotes changes without effecting locals
git checkout -b dev origin/dev  # create `dev` branch which tracks `origin/dev` and checkout to `dev`
```

### Remove Ignored But Already Tracked

from `main` branch

```sh
git rm -r --cached .
git add -A
git commit -m "Untrack ignored files"
git push
```
