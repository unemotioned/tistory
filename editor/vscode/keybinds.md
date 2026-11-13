# Keybinds

Open `Preferences: Open Keyboard Shortcuts (JSON)` with `Command Palette`

- Select suggestions with `Ctrl + J` / `Ctrl + K` (down/up)

- Accept with `Ctrl + Y`

- `Up` / `Down` arrows to act normally

- `Tab` to behave normally when suggestion window is open rather than just
  closing it

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
  // arrow keys close suggestions and act normally
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
  // behave as tab when suggestion window is open
  {
    "key": "tab",
    "command": "-acceptSelectedSuggestion",
    "when": "suggestWidgetHasFocusedSuggestion && suggestWidgetVisible && textInputFocus",
  },
  {
    "key": "tab",
    "command": "tabout",
    "when": "editorTextFocus && suggestWidgetVisible && !editorHasSelection && !editorHasMultipleSelections && !inSnippetMode && !inlineSuggestionVisible && !inlineEditIsVisible",
  },
]
```
