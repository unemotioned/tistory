# Tee

Copies standard input to standard output.

## Reference

- [10 Linux Tricks I WISH I Knew Snooner](https://www.youtube.com/watch?v=JjnICN3yW4E)

---

## The Problem

Not being able to write to root files even with `sudo`.

```sh
sudo echo "10.0.0.5 db" >> /etc/hosts
```

- `sudo` applies to `echo` ==> cannot edit the `/etc/hosts` file

---

## Usage

```sh
echo "10.0.0.5 db" | sudo tee -a /etc/hosts
```

- `sudo` applies to `tee`
- `tee`: `tee` take what got piped to it and writes to file
  - `-a`: append

> [!WARNING]
> Without `-a` flag for `tee` command it will overwrite the file with input.
