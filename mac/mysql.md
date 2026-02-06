# MySQL

## Table of Contents

- [Install](#install)
- [Initial Setup](#initial-setup)
- [Start Database](#start-database)
- [Connect to Root](#connect-to-root)
- [Create Database](#create-database)
- [Create User](#create-user)
- [Privileage](#privileage)

---

## Install

Homebrew:

```sh
brew install mysql@8.0

brew install --cask mysqlworkbench
```

> Install version 8 for competibility with workbench

---

## Initial Setup

- `~/.zshrc`: to use the mysql command

```sh
export PATH="/opt/homebrew/opt/mysql@8.0/bin:$PATH"
```

- `~/.zprofile`: for compilers to find mysql

```sh
export LDFLAGS="-L/opt/homebrew/opt/mysql@8.0/lib"
export CPPFLAGS="-I/opt/homebrew/opt/mysql@8.0/include"
```

To setup root user's PW and such run:

```sh
mysql_secure_installation
```

---

## Start Database

Check services:

```sh
brew services list | grep mysql
```

Start MySQL:

```sh
brew services start mysql@8.0
```

Stop MySQL:

```sh
brew services stop mysql@8.0
```

Restart MySQL:

```sh
brew services restart mysql@8.0
```

---

## Connect to Root

```sh
mysql -u root -p
```

Password in online

No space between `-p` option and password

```sh
mysql -u root -p{password}
```

---

## Create Database

```sql
CREATE DATABASE {database-name};
```

### List Databases

```sql
SHOW DATABASES;
```

### Show Current Database

```sql
SELECT DATABASE();
```

---

## Create User

```sql
CREATE USER '{username}'@'localhost' IDENTIFIED BY '{password}';
```

### List Users

```sql
SELECT user, host FROM mysql.user;
```

---

## Privileage

Grant every privileages on a specific DB

```sql
GRANT ALL PRIVILEGES ON {database_name}.* TO '{user_name}'@'localhost';
```

Apply Changes

```sql
FLUSH PRIVILEGES;
```

---

### Happy Hacking 🎉
