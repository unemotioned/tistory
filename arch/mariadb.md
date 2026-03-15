# MariaDB

Community-driven fork of MySQL,
created to stay open-source after Oracle acquired MySQL.

---

## Table of Contents

- [Setup](#setup)
- [Usage](#usage)
- [Commands](#commands)

---

## Setup

### Install

```sh
sudo pacman -S mariadb
```

### Initialize & Start

- `--user=mysql`: files are owned by the mysql system user
- `--basedir=/usr`: where MariaDB is installed on Arch (binaries and shared files)
- `--datadir=/var/lib/mysql`: where database files (tables, indexes) will be stored

```sh
sudo mariadb-install-db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
sudo systemctl enable --now mariadb
```

### Secure Installation

```sh
sudo mysql_secure_installation
```

---

## Usage

### Connect

```sh
mariadb -u root -p
```

### Create Database

```sql
CREATE DATABASE mydb;
```

### User & Grant Privileges

```sql
CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';

GRANT ALL PRIVILEGES ON mydb.* TO 'myuser'@'localhost';
FLUSH PRIVILEGES;
```

---

## Commands

### SQL

```sql
SHOW DATABASES;
SELECT user, host FROM mysql.user;
SHOW GRANTS FOR 'myuser'@'localhost';
DROP USER 'myuser'@'localhost';
DROP DATABASE mydb;
```

### Systemctl

```sh
sudo systemctl start mariadb # forget after reboot
sudo systemctl enable --now mariadb # run now + on every boot

sudo systemctl stop mariadb
sudo systemctl disable --now mariadb # stop now + no start on boot

systemctl status mariadb
```
