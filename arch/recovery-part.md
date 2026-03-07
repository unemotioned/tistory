# Windows Recovery Partition

How to remove `recovery` and "recover" the recovery partition

[Fix "Can't Extend C Drive with Unallocated Space" in Windows 10/11 - Techy Druid](https://www.youtube.com/watch?v=K76z0gQm9oA&list=WL&index=3)

---

## Table of Contents

- [Delete](#delete)
- [Recover](#recover)

---

## Delete

open `cmd prompt` with admin priviliege

```cmd
reagentc /disable

diskpart

list disk

sel disk 0

list part

sel part 4

detail part
```

copy the value of `Type` and `Attrib`

```cmd
del part override
```

---

## Recover

create 1GB of partition

from disk part select the create partition

### Set ID

```cmd
set id={copid-id-value}
```

### Set Attrib

```cmd
gpt attributes={copied-attirb-value}
```

### Remove Partition Letter

new recovery partition is visible from the file explorer

```cmd
list volume

sel volume D

remove letter=D

exit

reagentc /enable
```

---

## Trouble Shooting

copy past not working in cmd prompt

right click the title bar
check the use ctrl shift c/v for copy past
