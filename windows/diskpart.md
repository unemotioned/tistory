# Diskpart

## Table of Contents

- [Format USB](#format-usb)

---

## Format USB

```cmd
list disk

select disk <disk-no>

clean

create partition primary

select part 1

format fs=fat32 quick

assign

exit
```
