# [JetBrains](https://account.jetbrains.com/)

## Table of Contents

- [Shortcuts](#shortcuts)
- [Plugins](#plugins)
- [Settings](#settings)
  - [Tree Indent Guides](#tree-indent-guides)
  - [Inlay Usage & Code Author](#inlay-usage--code-author)
  - [Fold One-line Methods](#fold-one-line-methods)
  - [Caret Blink](#caret-blink)
  - [Open New Tab](#open-new-tab)
  - [Scroll Pass BOF](#scroll-pass-bof)
  - [Smooth Scrolling](#smooth-scrolling)
  - [Sticky Lines](#sticky-lines)
  - [Palantir Java Format](#palantir-java-format)
  - [Open with Single Click](#open-with-single-click)
  - [Memory Settings](#memory-settings)
  - [Markdown Smart Enter](#markdown-smart-enter)
  - [Completion Match Case](#completion-match-case)
- [Keymap](#keymap)
  - [Lookup](#lookup)

---

## Shortcuts

| No. | Action                     | Windows / Linux        | macOS                 |
| --- | -------------------------- | ---------------------- | --------------------- |
| 1   | Search Everywhere          | Shift + Shift          | -                     |
| 2   | Search File                | Ctrl + Shift + N       | Cmd + Shift + O       |
| 3   | Search Symbol              | Ctrl + Alt + Shift + N | Opt + Cmd + O         |
| 4   | Search Text                | Ctrl + Alt + Shift + E | Opt + Cmd + Shift + E |
| 5   | Run Everything             | Shift + F10            | Ctrl + Opt + R        |
| 6   | Project                    | Alt + 1                | Cmd + 1               |
| 7   | Run                        | Alt + 4                | Cmd + 4               |
| 8   | Problem                    | Alt + 6                | Cmd + 6               |
| 9   | Go to declaration or Usage | Ctrl + B               |                       |
| 10  | Go to implementations      | Ctrl + Alt + B         |                       |
| 11  | Rename                     | Shift + F6             | -                     |
| 12  | Format                     | Ctrl + Alt + L         | Opt + Cmd + L         |
| 13  | Generate Code              | Alt + Insert           | Cmd + N               |
| 14  | Next Error                 | F2                     | -                     |
| 15  | Prev Error                 | Shift + F2             | -                     |
| 16  | Show Context Actions       | Alt + Enter            | Opt + Enter           |

> [!NOTE]
> `-` means same.

---

## Plugins

- [IdeaVim](https://github.com/jetbrains/ideavim)
- [IdeaVim-Quickscope](https://plugins.jetbrains.com/plugin/19417-ideavim-quickscope)
- [IdeaVim-EasyMotion](https://plugins.jetbrains.com/plugin/13360-ideavim-easymotion/versions)
- [AceJump](https://github.com/acejump/AceJump)
- [Catppuccin Theme](https://plugins.jetbrains.com/plugin/18682-catppuccin-theme)
- [Atom Material Icons](https://plugins.jetbrains.com/plugin/10044-atom-material-icons)
- [Insepection Lens](https://plugins.jetbrains.com/plugin/19678-inspection-lens)

---

## Settings

### Tree Indent Guides

Settings > Appearance & Behavior > **Appearance** > _Tree Views_ > `Show indent guides`

### Inlay Usage & Code Author

Settings > Editor > **Inlay Hints** > _Code vision_ > `Usages`, `Code author`

### Fold One-line Methods

Settings > Editor > General > **Code Folding** > Fold by default: > _Java_ > `One-line methods`

### Caret Blink

Settings > Editor > General > **Appearance** > `Caret blinking (ms):`

### Open New Tab

Settings > Editor > General > **Editor Tabs** > _Tab Order_ > `Open new tabs at the end`

### Scroll Pass BOF

Settings > Editor > **General** > _Virtual Space_ > `Show virtual space at the bottom of the file`

### Smooth Scrolling

Settings > Editor > **General** > _Scrolling_ > `Enable smooth scrolling`

### Sticky Lines

Settings > Editor > **General** > _Sticky Lines_ > `Show sticky lines while scrolling`

### Palantir Java Format

1. Install the `palantir-java-format` plugin.
2. Settings > **Other Settings** > `Enable palantir-java-format Settings`

### Open with Single Click

Project window > 3 dot > Behavior > Open Files with Single Click, Open Directories with Single Click

> [!TIP]
> Try [Quick File Preview](https://plugins.jetbrains.com/plugin/12778-quick-file-preview) plugin for VSCode like behavior

### Memory Settings

Search `Change Memory Settings` from Actions (`Ctrl + Shift + A`) and change `Maximum Heap Size` to larger size to make IDE faster.

### Markdown Smart Enter

Autocompleting list item with `dash(-)` on new line.

Settings > Editor > General > **Smart Keys** > Markdown > _Lists_ > `Use Smart Enter and Backspace`

### Completion Match Case

Show suggestions even when case of letter doesn't match.

Settings > Editor > General > Code Completion > **Popup** > `Match case`

---

## Keymap

### Lookup

Same as auto suggestion or completion.

1. Settings > **Keymap** > Search `Lookup`
2. Remap `Choose Lookup Item Replace`, `Select Next Completion Option` and `Select Previous Completion Option` &rarr; `Ctrl` + `Y`, `J` and `K`

> [!NOTE]
> For some reason `Ctrl + Y` remap is not working.
