# Version

Change Java version when there is multiple JDKs installed.

## Table of Contents

- [macOS](#macos)
- [Arch](#arch)
- [Ubuntu](#ubuntu)

---

## macOS

Inside `.zprofile`:

Change the version number after `@`.

```sh
export PATH="/opt/homebrew/opt/openjdk@25/bin:$PATH"
export CPPFLAGS="-I/opt/homebrew/opt/openjdk@25/include"
```

Or declare it in variable:

```sh
java_version=25
export PATH="/opt/homebrew/opt/openjdk@${java_version}/bin:$PATH"
export CPPFLAGS="-I/opt/homebrew/opt/openjdk@${java_version}/include"
```

Update for current shell:

```sh
source ~/.zshrc
```

---

## Arch

Package Names:

- `jdk17-openjdk`
- `jdk21-openjdk`

Check current version:

```sh
archlinux-java status
```

Change version:

```sh
sudo archlinux-java set java-17-openjdk
```

---

## Ubuntu

Package Names:

- `openjdk-17-jdk`
- `openjdk-21-jdk`

Check installed:

```sh
sudo apt list --installed | grep openjdk
```

Change version:

```sh
sudo update-alternatives --config java

# java compiler separately
sudo update-alternatives --config javac
```
