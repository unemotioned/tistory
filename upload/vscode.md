# Visual Studio Code

## Table of Contents

- [터미널 명령어](#터미널-명령어)
- [키보드 단축키](#키보드-단축키)
- [확장 프로그램](#확장-프로그램)
  - [테마](#테마)
  - [폰트](#폰트)
- [유용한 설정](#유용한-설정)

---

## 터미널 명령어

VSCode 터미널에서 폴더/파일 만들고 열기

### 폴더 아이템 보기

```sh
ls
```

### 폴더로 이동

```sh
mkdir <폴더이름>

# 예시
mkdir basic
```

### 폴더 생성

```sh
mkdir <폴더이름>
```

### 파일 생성

```sh
New-Item -Path "<파일이름>" -ItemType File

# 또는
ni <파일이름>

# 예시
ni hello.js
```

### VSCode로 열기

#### 현재 폴더

현재 폴더에 대하여 새로운 VSCode 창을 연다

```sh
code .
```

#### 파일

VSCode 터미널에서 입력하면 현재 창에서 파일을 연다

```sh
code -r hello.js
```

> `-r`: `--reuse-window` 플래그의 약어

---

## 키보드 단축키

- open file: `ctrl + o`
- open folder: `ctrl + k, o`
- close folder: `ctrl + k, f`

- command palette: `ctrl + shift + p`
- terminal: `ctrl + backtick(grave)`
- new terminal: `ctrl + ~(tilde)`
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

- quick fix: `ctrl + .`
- comment: `ctrl + /`
- move line: `alt + arrow keys`
- rename symbols or file: `f2`

- select word at cursor: `ctrl + d`
- select every word at cursor: `ctrl + shift + l`
- select words: `ctrl + shift + left/right`

- multi cursor: `ctrl + left click`
- multi cursor vertical: `ctrl + shift + up/down`

- split window: `ctrl + \`
- change focus: `ctrl + 1`
- close pane: `ctrl + w`

- zen mode: `ctrl + k, z`

---

## 확장 프로그램

### Auto Close Tag

- HTML, XML 태그를 자동으로 닫아줌

### Auto Rename Tag

- 한쪽 태그 이름을 바꾸면 다른쪽도 바뀜

### CSS Peek

- HTML에서 정의 되어 있는 CSS를 확인 할 수 있음

### Code Runner

- 현재 파일을 `output` 창에서 실행: `ctrl + alt + n`

### Code Spell Checker

- 오타 검사

### ESLint

- JavaScript 에러를 `problems` 창에 표시

### JavaScript(ES6) code snippets

- JavaScript 추가 자동완성 제공

### Live Server (Five Server)

- HTML 파일을 localhost에서 열 수 있음

### Material Icon Theme

- 파일 트리의 폴더/파일 아이콘 변경

### Prettier

- HTML, CSS, JS, MD, Json ... 파일 포멧

- 현재 파일 포멧: `alt + shift + f`

### Quokka.js

Command palette에서 `Quokka.js: Start on Current File`를 선택하면 editor창에서
inline으로 결과를 보여줌

### Tabout

- 자동으로 닫히는 괄호/따옴표를 Tab키 넘어갈 수 있게 해줌

### npm Intellisense

- Node 패키지 자동완성 제공

---

### 테마

다음 테마중 하나 선택

- Catppuccin for VSCode (+ Catppuccin Icons for VSCode)
- GitHub Theme
- Nord
- One Dark Pro
- Rose Pine
- tokyo-night
- Vague Theme (Windsuf)

### 폰트

[nerdfonts](https://www.nerdfonts.com/)에서 다운로드 후 설치

Nerd font icons( 이런거), Ligature 지원

#### D2CodingLigature Nerd Font

- Naver에서 만듬, 한글 영어 특수문자간의 구별에 용이

#### JetBrainsMono Nerd Font

- 네모 반듯한 폰트

#### Iosevka Nerd Font

- 세로로 길쭉한 폰트

---

## 유용한 설정

Command palette에서 설정 이름을 검색해서 설정하거나
`Preference: Open User Settings (Json)`을 검색, `settgins.json`에서 직접 편집 할 수 있다.

```jsonc
{
  // HTML, CSS, JS 파일에서의 기본 들여쓰기 크기
  "editor.tabSize": 2,

  // Enter키로 자동완성 선택 비활성화
  "editor.acceptSuggestionOnEnter": "off",

  // != <= >= ==> 등을 더 재밋게 보여줌
  "editor.fontLigatures": true,
  "editor.fontFamily": "Iosevka Nerd Font",
  "terminal.integrated.fontFamily": "Iosevka Nerd Font",

  // 저장할때 자동으로 포멧
  "editor.formatOnSave": true,
  // 저장할때 동작
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit",
    "source.organizeImports": "explicit",
  },
  // 자동 저장 활성화
  "files.autoSave": "afterDelay",

  // 파일 트리 들여쓰기 크기
  "workbench.tree.indent": 16,
}
```
