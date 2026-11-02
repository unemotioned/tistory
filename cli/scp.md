# SCP

Move file / directory between local and SSH machine.

---

## File

From local to remote machine.

```sh
scp ~/myfolder/filename user@ip_addr:/path/to/destination/filename
```

Or change file name as you copy.

```sh
scp ~/myfolder/myfile user@ip_addr:/path/to/destination/filename
```

---

## Directory

Copy directory with the `recursive` flag.

```sh
scp -r ~/myfolder user@ip_addr:/path/to/destination/
```

---

## Remote to Local

Just flip the source and destination.

```sh
scp -r user@ip_addr:/path/to/destination/ ~/myfolder
```
