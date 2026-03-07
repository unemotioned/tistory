# Python Virtual Environment

- [create venv](#create-venv)
- [install modules](#install-modules)
- [deactivate](#deactivate)
- [aliases](#aliases)
- [freeze](#freeze)

## Install PIP

The python3 package manager

```sh
sudo apt install python3-pip
```

## Create venv

Create to desired location

```sh
python3 -m venv {dir/venv-name}
```

Activate venv

```sh
source {venv-path}/bin/activate
```

Update `pip` from inside the `venv`

```sh
sudo pip3 install --upgrade pip
```

## Install Modules

For example

```sh
pip3 install numpy
```

## Deactivate

```sh
deactivate
```

---

## Aliases

```sh
alias von=". {venv-path}/bin/activate"
alias voff="deactivate"
```

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

## Update

Update every modules inside venv

1. find outdated modules in freeze format
2. get the name only
3. update each one

```sh
pip list --outdated --format=freeze | cut -d= -f1 | xargs pip install -U
```
