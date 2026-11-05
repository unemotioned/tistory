# Reset Commit History

> [!WARNING]
> Nuclear launch detected.

```sh
git checkout --orphan tmp # new branch with no commit history
git add -A
git commit -m "first commit"
git branch -D main        # remove main branch
git branch -m main        # rename current branch to main
git push -f origin main   # force push
```
