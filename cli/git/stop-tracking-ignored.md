# Stop Tracking Ignored

After adding files to `.gitignore` which are already being tracked.

```sh
git rm -r --cached .
git add -A
git commit -m "untrack ignored"
git push
```
