# Shallow Clone

When cloning a super heavy project.

```sh
git clone --depth 1 <username>/<repository>

# or latest 100
git clone --depth 100 <username>/<repository>
```

Fetch rest of the commits.

```sh
git fetch --unshallow
```
