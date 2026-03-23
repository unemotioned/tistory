# Chromium

A web browser built for speed, simplicity and security

> You cannot even login to `chromium`

## Chromium VS Firefox

1. Chromium hides cursor automatically if needed when focus is changed to
   monkeytype or YouTbue. While firefox won't.

2. Chromium renders image faster then firefox.

3. Chromium has better GitHub markdown inline code fonts. (Thicker then firefox)

## Table of Contents

- [Install](#install)

- [Settings](#settings)

- [Favorites](#favorites)
  - [iCloud](#icloud)
  - [Naver](#naver)
  - [YouTube](#youtube)
  - [Claude](#claude)
  - [GitHub](#github)
  - [Monkeytype](#monkeytype)
  - [NSU](#nsu)
  - [LMS](#lms)

- [Extensions](#extensions)
  - [AdGuard AdBlocker](#adguard-adblocker)
  - [Unhook](#unhook)
  - [Vimium](#vimium)
  - [YouTube Auto HD + FPS](#youtube-auto-hd-fps)
  - [YouTube Auto Liker](#youtbue-auto-liker)

- [Remove Firefox](#remove-firefox)

---

## Install

Install from `extra` repository with `pacman`:

```sh
sudo pacman -S chromium
```

---

## Settings

- Appearance > Theme > `Dark`

- Show tab groups: off
- Show bookmarks bar: on

- Never translate Korean

---

## Favorites

### iCloud

### NAVER

- 설정
  - 화면 스타일
    - 다크 모드

### YouTube

- Settings
  - Playback and performance
    - Subtitles and Closed Captions: off
    - Browsing: Video previews: off

Ambient mode: off

### Claude

### GitHub

### Monkeytype

### Coupang

### NSU

### LMS

---

## Extensions

### AdGuard AdBlocker

- Allowlist
  - youtube.com

### Unhook

- Hide Home Feed: off

- Hide Video Side bar: off
  - Hide Live Chat: on
  - Hide Fundraiser: on

- Hide Shorts: on
- Hide Comments: on
- Hide Mixes: on
- Hide Explore, Trending: off

- Disable Autoplay: off
- Disable Annotations: off

### Vimium

### YouTube Auto HD + FPS

- Extension is on: on

- Use the same quality for all frame rates: on
- Use enhanced bitrate when it's the highest quality: on
- Use super resolution when available: on

- Run on YouTube Music: off

### YouTbue Auto Liker

- Enabled: on
- Subscribed Only: on
- Wait for Ads: off

---

## Remove Firefox

```sh
sudo pacman -Rns firefox
```

```sh
rm -rf ~/.cache/mozilla
rm -rf ~/.config/mozilla
```
