# Python Virtual Environment

## Table of Contents

- [Install PIP](#install-pip)
- [Create venv](#create-venv)
- [Activate venv](#activate-venv)
- [Install Modules](#install-modules)
- [Deactivate](#deactivate)
- [Freeze](#freeze)

---

## Install PIP

The python3 package manager

```sh
sudo apt install python3-pip
```

---

## Create venv

Create to desired location

```sh
python3 -m venv <dir/venv-name>
```

---

## Activate venv

For `bash` and `zsh`

```sh
source ~/venv/bin/activate
```

For `fish`

```sh
source ~/venv/bin/activate.fish
```

Update `pip` from inside the `venv`

```sh
sudo pip3 install --upgrade pip
```

---

## Install Modules

For example

```sh
pip3 install numpy
```

---

## Deactivate

```sh
deactivate
```

---

## Freeze

Save environment exactly

```sh
pip freeze > requirements.txt
```

Recreate env

```sh
pip install -r requirements.txt
```

Refreeze after upgrades for safety

```sh
pip install --upgrade requests
pip freeze > requirements.txt
```
