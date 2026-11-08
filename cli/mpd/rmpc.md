# [RMPC](https://github.com/mierak/rmpc)

Music player client written in Rust.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
  - [Start](#start)
  - [Pause](#pause)
  - [Rescane](#rescane)
- [Keybinds](#keybinds)
  - [Queue](#queue)
  - [Create Playlist](#create-playlist)
  - [Playlist Reorderl](#reorder-playlist)

---

## Install

```sh
sudo pacman -Syu rmpc
```

---

## Usage

### Start

```sh
rmpc
```

### Pause

```sh
rmpc pause
```

Or kill `mpd` process:

```sh
pkill mpd
```

> [!NOTE]
> You must restart the `mpd` manually after this to listen to this again.

### Rescane

Rescan music library after downloading music or relocating them.

```sh
rmpc rescane
```

---

## Keybinds

### Queue

- `a`: Add a song at cursor
- `A`: Add whole playlist

### Create Playlist

1. Search song from `Search` tab
2. `Ctrl + S, A`
3. Create new or add to existing one

### Reorder Playlist

- Move down

```txt
Shift + J
```

- Move up

```txt
Shift + K
```

- Select Multiple:

```txt
Space
```
