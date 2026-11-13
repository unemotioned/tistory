# Settings

Open `Preference: Open User Settings (JSON)` with **Command Palette**.

```jsonc
{
  // indent width
  "editor.tabSize": 4,
  // settings for specific filetype
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.tabSize": 2,
  },

  /* Do not accept suggestion other then Tab key */
  // disable . (dot)
  "editor.acceptSuggestionOnCommitCharacter": false,
  // disable Enter
  "editor.acceptSuggestionOnEnter": "off",

  // enable ligatures for != <= >= ==>
  "editor.fontLigatures": true,
  "editor.fontFamily": "Iosevka Nerd Font",
  "terminal.integrated.fontFamily": "Iosevka Nerd Font",

  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit",
    "source.organizeImports": "explicit",
  },

  "workbench.tree.indent": 16,

  // do not make any sound
  "accessibility.signalOptions.volume": 0,

  // cleaner UI
  "breadcrumbs.enabled": false,
  "editor.stickyScroll.enabled": false,

  // always add EOL
  "files.insertFinalNewline": true,
  // dim EOL line number
  "editor.renderFinalNewline": "dimmed",

  "window.openFilesInNewWindow": "on",
}
```
