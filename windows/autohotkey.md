# AutoHotkey

[autohotkey.com](https://www.autohotkey.com/)

Software level keyboard remapping

---

## Remap CapsLock

`CapsLock` to `ESC` when tapped and `Ctrl` when held

Tap timeout is 0.2 seconds

> Version 2 syntax

```ahk
*CapsLock::
{
    if KeyWait("CapsLock", "T0.2")
    {
        Send "{Esc}"
    }
    else
    {
        Send "{Ctrl down}"
        KeyWait "CapsLock"
        Send "{Ctrl up}"
    }
}
```

---

## Run On Startup

Open Run dialog with `Win + R`

Type `shell:startup` and Enter to open Startup folder

Put the script in this folder
