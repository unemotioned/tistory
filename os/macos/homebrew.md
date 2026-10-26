# [Homebrew](https://brew.sh/)

Package manager for macOS.

## Table of Contents

- [Install Homebrew](#install-homebrew)
- [Usage](#usage)
  - [Etc](#etc)
- [Dependency](#dependency)
  - [Reverse Dependency](#reverse-dependency)
  - [Remove Orphaned](#remove-orphaned-packages)
- [Pin Package Version](#pin-package-version)
  - [Unpin Package](#unpin-package)
- [Save Installed Packages](#save-installed-packages)
- [Tap](#tap)

---

## Install Homebrew

Execute the following command in the terminal:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Add Homebrew to `PATH` (change the user name to yours):

```sh
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/unemotioned/.zprofile
&& eval "$(/opt/homebrew/bin/brew shellenv)"
```

Or copy it from the installation prompt.

Check if installed:

```sh
brew --version
```

---

## Usage

```sh
brew search <pkg>

brew list

brew install <pkg>

brew uninstall <pkg>

# update package index
brew update

# update outdated packages
brew upgrade
```

### Etc

```sh
# clear cache
brew cleanup

# check homebrew health
brew doctor
```

---

## Dependency

Dependencies of package

```sh
brew deps <pkg>

brew deps --tree <pkg>
brew deps --recursive <pkg>
```

### Reverse Dependency

Packages that depends on a package.

```sh
brew uses <pkg>
```

### Remove Orphaned Packages

```sh
brew autoremove --dry-run
brew autoremove
```

---

## Pin Package Version

Keep `brew upgrade` from updating the package:

```sh
brew pin openjdk@17
```

Show the pinned packages with the `--pinned` flag:

```sh
brew list --pinned
```

Or list outdated packages before `upgrade`:

```sh
brew outdated
```

### Unpin Package

```sh
brew unpin openjdk@17
```

---

## Save Installed Packages

Create a `Brewfile` where the command was executed:

```sh
brew bundle dump
```

To install with a `Brewfile`, run from the `Brewfile` file path:

```sh
brew bundle install
```

---

## Tap

Commands for third-party taps.

### List All Taps

```sh
brew tap
```

### Add Tap

```sh
brew tap <username>/<repository>
```

### Remove Tap

```sh
brew untap <username>/<repository>
```

### Trust Tap

```sh
brew trust <username>/<repository>
```
