# Advanced Package Tool

## List of Content

- [Before Use](#before-use)
- [How to Use](#how-to-use)
- [Info](#info)
- [Flags](#flags)
- [Cleanup](#cleanup)
- [Fix Install](#fix-install)

---

## Before Use

- `sudo`: Super User Do
  - install, remove, update
  - modifying sys files(/etc, /usr, /bin, ...)
  - managing services
  - changing user

Update apt

```sh
sudo apt update
```

Checkout outdated packages first

```sh
apt list --upgradeable
```

Update outdated pkg

```sh
sudo apt upgrade
```

Keep pkg from automatically updated

```sh
sudo apt-mark hold openjdk-17-jdk
```

Use `unhold` to undo mark

---

## How To Use

You can pass more then one argument

```sh
sudo apt install {pkg} {pkg} ...
```

---

## Info

### Search

Update the APT local cache

```sh
sudo apt update
```

Search for package interactively

```sh
apt-cache search . | fzf
```

`List` out installed packages

```sh
apt list --installed
```

Use `show` flag to show package details

---

## Flags

`--yes` or `-y`: automatic yes

`--quiet` or `-q`: quieter output

`--no-install-recommends` or `--no-install-reco`

`--reinstall`

`--purge`

---

## Cleanup

- `autoremove`: remove unused dependencies
- `clean`: clear download cache

```sh
sudo apt autoremove
sudo apt clean
```

---

## Fix Install

### Fix Broken Dependencies

```sh
sudo apt install -f
```

### Check not being upgraded

```sh
sudo apt dist-upgrade -a
```

You may install the package separated

### Run Final Upgrade

```sh
sudo apt full-upgrade -y
```
