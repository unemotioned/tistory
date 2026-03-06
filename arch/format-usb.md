# Formatting USB

from iso usb to normal usb stick

```sh
lsblk
```

Example of USB:

```sh
NAME        MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda           8:0    1 114.6G  0 disk
├─sda1        8:1    1   6.2G  0 part
├─sda2        8:2    1     5M  0 part
├─sda3        8:3    1   300K  0 part
└─sda4        8:4    1 108.4G  0 part
```

Unmount all partitions

```sh
sudo umount /dev/sda*
```

Wipe and create new partition table

```sh
sudo fdisk /dev/sda
```

1. press `g` ==> new GPT partition
2. press `n` ==> new partition
3. Enter 3 times ==> usb into one partition
4. press `w` ==> write and exit

Install `exfatprogs` if not already installed:

```sh
sudo pacman -S exfatprogs
```

Format the partition:

```sh
sudo mkfs.exfat /dev/sda1
```
