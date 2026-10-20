# Powershell

Windows powershell commands. Which is different from `CMD`.

## Table of Contents

- [Get Child](#get-child)
- [Set Location](#set-location)
- [New](#new)
- [Rename](#rename)
- [Move](#move)
- [Remove](#remove)
- [Copy](#copy)

---

## Get Child

List folders and files inside current path.

```powershell
Get-ChildItem

dir # alias
ls # unix alias
```

---

## Set Location

Move into other folder.

```powershell
Set-Location "C:\there" # absolute path

# unix alias
cd "what\is\there"

cd ..     # move to parent folder
cd ../..  # move to parent's parent
cd ../foo # go to folder next to current folder

pwd # print working directory
```

---

## New

Create new folder or file.

- **Folder**

```powershell
New-Item -ItemType Directory -Path "new-folder"

# alias
mkdir new-folder
```

- **File**

```powershell
New-Item -ItemType File -Path "new-file.txt"

# alias
ni new-file.txt
```

> [!IMPORTANT]
> Argument for `-ItemType` option if different.

---

## Rename

```powershell
Rename-Item "before" "after"

# alias
ren "before" "after"

# same for file
ren "before.txt" "after.txt"
```

> [!NOTE]
> No `-Recurse` flag needed when renaming folder.

---

## Move

Relocate folder or file to another path.

```powershell
Move-Item "original-path" "new-path"

# alias
mv "original-path" "new-path"
```

---

## Remove

- **Folder**
  - `-Recurse`: for none-empty folder
  - `-Force`: hidden/read-only files

```powershell
Remove-Item "C:\path\to\folder" -Recurse -Force

# alias
rm "C:\path\to\folder" -Recurse -Force
```

- **File**

```powershell
rm "file-name.txt"

rm "file-name.txt" -Force # if hidden/read-only
```

---

## Copy

```powershell
Copy-Item "C:\source\folder" "C:\destination" -Recurse

# alias
cp "C:\source\folder" "C:\destination" -Recurse
```

Copy file without `-Recurse` flag.
