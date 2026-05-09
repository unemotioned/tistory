# Nodemon

Watch files for change and execute a command

---

## Installation

Install with npm

```sh
sudo npm install --global nodemon
```

### Update

```sh
npm update nodemon
```

---

## Configuration

Create `nodemon.json` at where you will run `nodemon` command

- `watch`: Files or directories to monitor
- `ext`: File extensions to watch
- `ignore`: Path to exclude
- `exec`: Command to run on changes
- `start`: Command to run on start before `exec`

```json
{
  "watch": ["*.py"],
  "ext": "py",
  "ignore": [],
  "exec": "python3 ./binary_tree.py",
  "events": {
    "start": "clear"
  }
}
```

---

## Use

Just run:

```sh
nodemon
```
