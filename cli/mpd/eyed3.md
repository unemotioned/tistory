# eyeD3

Editing `ID3` metadata of MP3 file.

## Reference

[readthedoc - eyed3](https://eyed3.readthedocs.io/)

## Table of Contents

- [Install](#install)
- [Metadata](#metadata)
- [Album Art](#album-art)

---

## Install

```sh
yay -Syu python-eyed3
```

---

## Metadata

Edit metadata of `<file-name>` file:

```sh
eyeD3 --title "<my-title>" --artist "<artist-name>" --album "<album>" <file-name>
```

- `--title`: Title of the music.
- `--artist`: Author of the music.
- `--album`: Album the music belongs to.

Now you can search from `rmpc` with tags.

---

## Album Art

Download a album art first.

```sh
eyeD3 --add-image "<cover.jpg:FRONT_COVER>" <file-name>
```

Set `cover.jgp` as album art of `<file-name>`.

> [!TIP]
> Default album art view limit is `1200x1200`. Change image size with
> [imagemagick.md](../imagemagick.md).
