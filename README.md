# Machine-Setup

How to setup my machines

- Mac OS
  - Aerospace

- Arch Linux
  - Hyprland

- Ubuntu
  - i3

- Neovim
- ZSH

---

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
git checkout --orphan temp_branch # new branch with no commit history
git add -A
git commit -m "Initial commit"
git branch -D main # remove main branch
git branch -m main # rename current branch to main
git push -f origin main # force push
```
