# Pacman

How to use the package manager for Arch.

## Reference

- [ArchWiki](https://wiki.archlinux.org/title/Pacman)

## Table of Contents

- [Install](#install)
- [Update](#update)
- [Remove](#remove)
  - [Remove orphaned](#remove-orphaned)
  - [Remove Dependencies](#remove-dependencies)
  - [Remove Parent Package](#remove-parent-package)
- [Search](#search)
  - [From Database](#from-database)
  - [From Installed](#from-installed)
- [Clear Cache](#clear-cache)

---

## Install

```sh
# normal install
sudo pacman -S vim

# without confirmation
sudo pacman -S --noconfirm neovim

# if not already installed
sudo pacman -S --needed emacs
```

---

## Update

```sh
# full upgrade (recommended)
sudo pacman -Syu

# force fresh pkg db download
sudo pacman -Syyu
```

> [!TIP]
> Reboot is recommended for upgrades to upply to the system.

Recommended way to install packages:

```sh
sudo pacman -Syu <pkg-name>
```

> [!WARNING]
> Partial upgrade is not recommended.

```sh
sudo pacman -Sy <pkg-name>
```

---

## Remove

```sh
# specified package
sudo pacman -R nano

# with dependencies
sudo pacman -Rs nano

# with dependencies and config files
sudo pacman -Rns code
```

### Remove Orphaned

List orphaned:

- `Q`: query
- `t`: orphaned packages
- `d`: dependency only
- `q`: quiet output

```sh
pacman -Qtdq
```

- Remove orphaned with queried results:

```sh
sudo pacman -Rns $(pacman -Qtdq)
```

### Remove Dependencies

List dependent packages:

```sh
pacman -Qi <pkg-name>
```

### Remove Parent Package

Remove without dependency check.

```sh
sudo pacman -Rdd <pkg-name>
```

- `-d`: Skip dependency check
- `-dd`: Skip all dependency check

---

## Search

### From Database

```sh
pacman -Ss <pkg-name>
```

### From Installed

```sh
# query every installed packages
pacman -Q

# explicitly installed
pacman -Qe

# dependency only
pacman -Qd
```

---

## Clear Cache

```sh
# remove outdated
sudo pacman -Sc

# remove all cached packages
sudo pacman -Scc
```
