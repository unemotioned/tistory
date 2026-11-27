# SSH into install environment

How to SSH into live install environment.

## Table of contents

- [Connect to wifi](#connect-to-wifi)
- [Set root password](#set-root-password)
- [Start ssh server](#start-ssh-server)
- [SSH from another machine](#ssh-from-another-machine)

---

## Connect to wifi

Connect using `iwd`:

```sh
# enter iwctl shell
iwctl

# get your wifi device name
device list # example: wlan0

# init scan
station wlan0 scan

# list available networks
station wlan0 get-networks

# connect
station wlan0 connect <SSID>

# enter passphrase

exit
```

Test connection:

```sh
ping -c 4 archlinux.org
```

- `-c 4`: stop after sending 4 packets

---

## Set root password

```sh
passwd
```

---

## Start ssh server

Check ssh server daemon status:

```sh
systemctl status sshd
```

Start ssh server:

```sh
systemctl start sshd
```

Get current machine's IP address:

```sh
ip -c -br -4 addr
```

- `-c`: color
- `-br`: brief
- `-4`: IPv4 address
- `addr`: address show

Output:

```text
lo          UNKNOWN      127.0.0.1/8
wlan0       UP           192.168.0.45/24 metric 600
```

IP address with `UP` status is the one.

---

## SSH from another machine

```sh
ssh root@192.168.0.25
```

1. accept host fingerprint if need to
2. enter root password of machine you ssh into
