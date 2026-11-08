# [YT DLP](https://github.com/yt-dlp/yt-dlp)

A feature-rich command-line video/audio downloader.

## Table of Content

- [Install](#install)
- [Download](#download)
- [Extract Audio](#extract-audio)
- [Config](#config)

---

## Install

```sh
sudo pacman -Syu yt-dlp
```

---

## Download

```sh
yt-dlp "<video-url>"
```

Example:

<!-- yt-dlp https://www.youtube.com/watch?v=jNQXAC9IVRw -->

```sh
yt-dlp https://www.youtube.com/watch?v=dQw4w9WgXcQ
```

> [!TIP]
> Play it once to check the quality.

### Flag

Use `-k` flag to keep both **WEBM** and **MP4**.

```sh
yt-dlp <video-url> -k
```

---

## Extract Audio

```sh
yt-dlp -x --audio-format mp3 "<URL>"
```

- `-x`: Extract audio.
- `--audio-format`: Specify filetype.

---

## Config

To guarantee output in **MP4** format.

Inside `~./config/yt-dlp/config`:

```txt
-f "bv[ext=mp4]+ba[ext=m4a]/b[ext=mp4]"
--merge-output-format mp4
```

And just run:

```sh
yt-dlp "<video-url>"
```
