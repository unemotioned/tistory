# [JetBrains](https://account.jetbrains.com/)

## Table of Contents

- [Shortcuts](#shortcuts)
- [Plugins](#plugins)
- [Settings](#settings)
  - [1. Tree Indent Guides](#1-tree-indent-guides)
  - [2. Inlay Usage & Code Author](#2-inlay-usage--code-author)
  - [3. Fold One-line Methods](#3-fold-one-line-methods)
  - [4. Caret Blink](#4-caret-blink)
  - [5. Open New Tab](#5-open-new-tab)
  - [6. Scroll Pass BOF](#6-scroll-pass-bof)
  - [7. Smooth Scrolling](#7-smooth-scrolling)
  - [8. Sticky Lines](#8-sticky-lines)
  - [9. Markdown Smart Enter](#9-markdown-smart-enter)
  - [10. Completion](#10-completion)
  - [11. Light Bulb](#11-light-bulb)
  - [12. Open with Single Click](#12-open-with-single-click)
  - [13. Memory Settings](#13-memory-settings)
  - [14. Palantir Java Format](#14-palantir-java-format)
- [Keymap](#keymap)
  - [Lookup](#lookup)

---

## Shortcuts

| No. | Action               | Windows / Linux            | macOS                      |
| --- | -------------------- | -------------------------- | -------------------------- |
| 1   | Search Everywhere    | `Shift + Shift`            | -                          |
| 2   | Search File          | `Ctrl + Shift + N`         | `Cmd + Shift + O`          |
| 3   | Search Symbol        | `Ctrl + Alt + Shift + N`   | `Opt + Cmd + O`            |
| 4   | Search Text          | `Ctrl + Alt + Shift + E`   | `Opt + Cmd + Shift + E`    |
| 5   | Run Everything       | `Shift + F10`              | `Ctrl + Opt + R`           |
| 6   | Project              | `Alt + 1`                  | `Cmd + 1`                  |
| 7   | Run                  | `Alt + 4`                  | `Cmd + 4`                  |
| 8   | Problems             | `Alt + 6`                  | `Cmd + 6`                  |
| 9   | Go to Declaration    | `Ctrl + B`                 | `Cmd + B`                  |
| 10  | Find Usages          | `Ctrl + Alt + F7`          | `Opt + Cmd + F7`           |
| 11  | Rename               | `Shift + F6`               | -                          |
| 12  | Format               | `Ctrl + Alt + L`           | `Opt + Cmd + L`            |
| 13  | Generate Code        | `Alt + Insert`             | `Cmd + N`                  |
| 14  | Show Context Actions | `Alt + Enter`              | `Opt + Enter`              |
| 15  | Next Error           | `F2`                       | -                          |
| 16  | Prev Error           | `Shift + F2`               | -                          |
| 17  | Next Change          | `Ctl + Alt + Shift + Up`   | `Opt + Cmd + Shift + Up`   |
| 18  | Prev Change          | `Ctl + Alt + Shift + Down` | `Opt + Cmd + Shift + Down` |

> [!NOTE]
> `-` means same.

---

## Plugins

- [1. AceJump](https://github.com/acejump/AceJump)
- [2. Atom Material Icons](https://plugins.jetbrains.com/plugin/10044-atom-material-icons)
- [3. Catppuccin Icons](https://plugins.jetbrains.com/plugin/23029-catppuccin-icons)
- [4. Catppuccin Theme](https://plugins.jetbrains.com/plugin/18682-catppuccin-theme)
- [5. IdeaVim](https://github.com/jetbrains/ideavim)
- [6. IdeaVim-EasyMotion](https://plugins.jetbrains.com/plugin/13360-ideavim-easymotion/versions)
- [7. IdeaVim-Quickscope](https://plugins.jetbrains.com/plugin/19417-ideavim-quickscope)
- [8. IdeaVimExtension](https://plugins.jetbrains.com/plugin/9615-ideavimextension)
- [9. Inspection Lens](https://plugins.jetbrains.com/plugin/19678-inspection-lens)
- [10. palantir-java-format](https://plugins.jetbrains.com/plugin/13180-palantir-java-format)

---

## Settings

### 1. Tree Indent Guides

Settings > Appearance & Behavior > **Appearance** > _Tree Views_ > enable `Show indent guides`

---

### 2. Inlay Usage & Code Author

Settings > Editor > **Inlay Hints** > _Code vision_ > `Usages`, `Code author`

---

### 3. Fold One-line Methods

Settings > Editor > General > **Code Folding** > Fold by default: > _Languages_ > disable `One-line methods`

---

### 4. Caret Blink

Settings > Editor > General > **Appearance** > disable `Caret blinking (ms):`

---

### 5. Open New Tab

Settings > Editor > General > **Editor Tabs** > _Tab Order_ > enable `Open new tabs at the end`

---

### 6. Scroll Pass BOF

Settings > Editor > **General** > _Virtual Space_ > enable `Show virtual space at the bottom of the file`

---

### 7. Smooth Scrolling

- `Scroll wheel`: Settings > Appearance & Behavior > Appearance > _UI Options_ > disable `Smooth scrolling`
- `Arrow keys`: Settings > Editor > **General** > _Scrolling_ > disable `Enable smooth scrolling`

---

### 8. Sticky Lines

Settings > Editor > **General** > _Sticky Lines_ > disable `Show sticky lines while scrolling`

---

### 9. Markdown Smart Enter

Autocompleting list item with `dash(-)` on new line.

Settings > Editor > General > **Smart Keys** > Markdown > _Lists_ > disable `Use Smart Enter and Backspace`

---

### 10. Completion

- Show suggestions even when case of letter doesn't match.

Settings > Editor > General > Code Completion > **Popup** > disable `Match case`

- Always show type-matching completion

Settings > Editor > General > Code Completion > **Popup**

1. disable `Basic Completion`
2. remap `Type-Matching Completion` to **Ctrl+Space**

---

### 11. Light Bulb

Settings > Editor > General > Appearance > _Code Assistance_ > disable `Show intension bulb`

---

### 12. Open with Single Click

Project window > 3 dot > Behavior > Open Files with Single Click, Open Directories with Single Click

> [!TIP]
> Try `Enable Preview Tab` option for VSCode like behavior

---

### 13. Memory Settings

Search `Change Memory Settings` from Actions (`Ctrl + Shift + A`) and change `Maximum Heap Size` to larger size to make IDE faster.

---

### 14. Palantir Java Format

1. Install the `palantir-java-format` plugin.
2. Settings > **Other Settings** > `Enable palantir-java-format Settings`

---

## Keymap

### Lookup

Same as auto suggestion or completion.

1. Settings > **Keymap** > Search `Lookup`
2. Remap `Choose Lookup Item Replace`, `Select Next Completion Option` and `Select Previous Completion Option` &rarr; `Ctrl` + `Y`, `J` and `K`
3. Remove `Tab` from `Choose Lookup Item Replace` (tab to work normally even when suggestion is opened)

If `Ctrl + K` for lookup is not working:

Settings > Editor > Vim > Find **Ctrl+K** from `Shortcuts` and change the `Handler` to **IDE**
