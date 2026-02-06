# MySQL

## Table of Contents

- [Install](#install)
- [Initial Setup](#initial-setup)
- [Start Database](#start-database)
- [Connect to Root](#connect-to-root)
- [Create Database](#create-database)
- [Create User](#create-user)
- [Privilege](#privilege)

---

## Install

Homebrew:

```sh
sudo apt install mysql-server mysql-client mysql-common
```

---

## Initial Setup

```sh
sudo mysql_secure_installation
```

Say `n` to the first one which is password validation
and all the others to `yes`

---

## Start Database

Check services:

```sh
systemctl status mysql
```

Start MySQL:

```sh
systemctl start mysql
```

Stop MySQL:

```sh
systemctl stop mysql
```

Restart MySQL:

```sh
systemctl restart mysql
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

## Privilege

Grant every privilege on a specific DB

```sql
GRANT ALL PRIVILEGES ON {database_name}.* TO '{user_name}'@'localhost';
```

Apply Changes

```sql
FLUSH PRIVILEGES;
```

---

### Happy Hacking 🎉
