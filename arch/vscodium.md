# Visual Studio Codium

Microsoft VSCode with no telementary feature

## Table of Contents

- [Install](#install)
- [Terminal Commands](#terminal-commands)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Extensions](#extensions)
- [Keybindings.json](#keybindingsjson)

---

## Install

```sh
yay -S codium-bin
```

---

## Terminal Commands

open codium

```sh
codium
```

### From The VSCode Terminal

`-r`: reuse-window

```sh
codium -r <file-name>
```

---

## Keyboard Shortcuts

- open file: `ctrl + o`
- open folder: `ctrl + k, o`
- close folder: `ctrl + k, f`

- command prompt: `ctrl + shift + p`
- terminal: `ctrl + backtick(tilde)`
- new terminal: `ctrl + ~`
- problems: `ctrl + shift + m`
- toggle file explorer: `ctrl + shift + e`
- search file: `ctrl + p`
- search workspace symbols: `ctrl + shift + o`
- search file symbols: `ctrl + t`

- front of line: `home`
- end of line: `end`
- move by word: `ctrl + arrow keys`

- go to definition: `ctrl + left click`

- file search replace: `ctrl + f`
- workspace search replace: `ctrl + shift + f`

- format: `ctrl + shift + i`
- quick fix: `ctrl + .`
- comment: `ctrl + /`
- move line: `alt + arrow keys`
- rename symbols or file: `f2`

- select word at cursor: `ctrl + d`
- select every word at cursor: `ctrl + shift + l`
- select words: `ctrl + shift + left/right`

- multi cursor: `ctrl + left click`
- multi cursor vertical: `ctrl + shift + up/down`

- run code: `ctrl + alt + n`

- split window: `ctrl + \`
- change focus: `ctrl + 1`
- close pane: `ctrl + w`

- zen mode: `ctrl + k, z`

---

## Extensions

### Node.js

- Auto Close Tag
- Auto Rename Tag
- CSS Peek
- ESLint
- JavaScript(ES6) code snippets
- Live Server (Five Server)
- Prettier - Code formatter
- npm Intellisense
- Quokka.js

### General

- Bracket Pair Color DLW
- Code Runner
- Code Spell Checker
- Markdown Preview Enhanced
- markdownlint
- Tabout

### ETC

- Material Icon Theme
- One Dark Pro (One Dark Pro Mix)

### I Use Neovim BTW

- Neovim

---

## Keybindings.json

- Select suggestions with ctrl + j, k
- Accept with ctrl + y
- Disable up/down arrow keys

```jsonc
// Place your key bindings in this file to override the defaults
[
  // select suggestions with ctrl + j and K
  {
    "key": "ctrl+j",
    "command": "selectNextSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus",
  },
  {
    "key": "ctrl+k",
    "command": "selectPrevSuggestion",
    "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus",
  },
  // accept suggestion with ctrl + y
  {
    "key": "ctrl+y",
    "command": "acceptSelectedSuggestion",
    "when": "suggestWidgetVisible && textInputFocus",
  },
  // disable arrow keys from selecting suggestions
  {
    "key": "down",
    "command": "runCommands",
    "args": { "commands": ["hideSuggestWidget", "cursorDown"] },
    "when": "suggestWidgetVisible && textInputFocus",
  },
  {
    "key": "up",
    "command": "runCommands",
    "args": { "commands": ["hideSuggestWidget", "cursorUp"] },
    "when": "suggestWidgetVisible && textInputFocus",
  },
]
```
