# [MPD](https://www.musicpd.org/)

Music Player Daemon.

## Reference

[the dream music player, finally. - Bread on Penguins](https://www.youtube.com/watch?v=oTOu7VfXnl8)

---

## Installation

```sh
sudo pacman -Syu mpd
```

--

## Config

Inside `~/.config/mpd/mpd.conf`:

```conf
music_directory    "/home/unemotioned/Music/"
playlist_directory "/home/unemotioned/Music/Playlists/"
db_file            "/home/unemotioned/.local/share/mpd/database"

auto_update     "yes"
bind_to_address "127.0.0.1"
restore_paused  "yes"

audio_output {
    type "pipewire"
    name "PipeWire"
}
```

---

1. Download music with [yl-dp](./yt-dlp.md)

2. Edit metadata with [eyed3](./eyed3.md)
   - Set album art for **M4A**(Apple Music) with
     [atomicparley](./atomicparsley.md)

3. Create playlist and play them with [rmpc](./rmpc.md)
