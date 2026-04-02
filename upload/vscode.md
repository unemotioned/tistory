# Visual Studio Code

Microsoft에서 [Typescript](https://www.typescriptlang.org/)로 만든 무료 텍스트 편집기

[GitHub](https://github.com/) 계정을 연동해서 설정, 확장프로그램 등을 연동할 수 있음

## Table of Contents

- [터미널 명령어](#터미널-명령어)
- [키보드 단축키](#키보드-단축키)
  - [폴더/파일 열기/닫기](#폴더파일-열기닫기)
  - [탭 관리](#탭-관리)
  - [패널 관리](#패널-관리)
  - [텍스트 편집](#텍스트-편집)
  - [커서](#커서)
  - [심볼](#심볼)
  - [좋은거](#좋은거)
- [확장 프로그램](#확장-프로그램)
  - [테마](#테마)
  - [폰트](#폰트)
- [유용한 설정](#유용한-설정)

---

## 터미널 명령어

VSCode 터미널에서 폴더/파일 만들고 열기

### 폴더 아이템 보기

List

```sh
ls
```

### 폴더로 이동

Change Directory

> Directory: 경로

```sh
cd <폴더이름>

# 예시)
cd basic/ch01
```

### 폴더 생성

Make Directory

```sh
mkdir <폴더이름>
```

### 파일 생성

```sh
New-Item -Path "<파일이름>" -ItemType File

# 또는
ni <파일이름>
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

> `-r`: `--reuse-window` (option)flag 약어

---

## 키보드 단축키

- [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [macOS](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Linux](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)

윈도우 용 단축키 정리

- 모든 단축키 보기: `ctrl + k, s`

### 폴더/파일 열기/닫기

- 파일 열기: `ctrl + o`
- 폴더 열기: `ctrl + k, o`
- 최근 폴더/파일 열기: `ctrl + r`
- 폴더 닫기: `ctrl + k, f`

### 탭 관리

- 탭 닫기: `ctrl + w`
- 모든 탭 닫기: `ctrl + shift + w` / `ctrl + k, w`
- 닫은 탭 다시 열기: `ctrl + shift + t`
- 탭을 여러 패인으로 나누기: `ctrl + alt + left/right arrow`
- 현재 탭을 좌우로 복사: `ctrl + \`
- 열린 탭에서 이동: `ctrl + tab`
- 패널 선택: `ctrl + 1/2/3 ...`

### 패널 관리

- 터미널: `ctrl + backtick(grave)`
- 새 터미널: `ctrl + ~ (tilde)`
- 파일 검색: `ctrl + p`
- Command Palette: `ctrl + shift + p`
- 사이드바 토글: `ctrl + b`
- 파일 트리: `ctrl + shift + e`
- problems 패널: `ctrl + shift + m`
- output 패널 : `ctrl + shift + u`

### 텍스트 편집

- 주석 처리: `ctrl + /`
- 뒤로가기 취소: `ctrl + shift + z` / `ctrl + y`
- 커서의 문자와 일치하는 모든 문자 선택: `ctrl + d`
- 들어쓰기 + : `]` / (줄의 가장 앞에서)`tab`
- 들여쓰기 - : `[` / (줄의 가장 앞에서)`shift + tab`
- 현재 줄 삭제: `ctrl + shift + k`
- 줄아래 새로운 줄: `ctrl + enter`
- 줄위에 새로운 줄: `ctrl + shift + enter`
- 줄 이동: `alt + up/down arrow`
- 줄 복사: `alt + shift up/down arrow`
- quickfix: `ctrl + .(온점)`
- 파일 포멧: `alt + shift + f`

- 문자열 찾기: `ctrl + f`
- 찾은 문자열 바꾸기: `ctrl + h`

- 워크스패이스에서 문자열 찾기: `ctrl + shift + f`
- 워크스패이스에서 찾은 문자열 바꾸기: `ctrl + shift + h`

### 커서

- 줄 가장 앞으로: `home`
- 줄 가장 뒤로: `end`
- 단어 단위로 이동: `ctrl + left/right arrow`
- 단어 단위로 이동 + 선택: `ctrl + shift + left/right arrow`
- 위/아래 커서 추가: `ctrl + alt + up/down arrow`
- 커서 추가: `alt + left click`

### 심볼

Symbol: 변수/함수 이름

이름 변경: `f2`
현재 파일에서 검색: `ctrl + shift + o`
workspace에서 검색: `ctrl + t`

선언된 위치로 가기: `f12` / `ctrl + left click`
선언된 부분 훔쳐보기: `alt + f12`

변수/함수 사용된 곳으로 이동: `shift + f12`
변수/함수 사용된 곳 전부 표시: `alt + shift + f12`

### 좋은거

- 에디터 창만 보기: `ctrl + k, z`
- Editor 창 중앙 정렬: Command Palette &rarr; `View: Toggle Centered Layout`
- 새로고침: Command Palette &rarr; `Developer: Reload Window`

---

## 확장 프로그램

확장프로그램 사이드바 단축키: `ctrl + shift + x`

### Auto Close Tag

- HTML, XML 태그를 자동으로 닫아줌

### Auto Rename Tag

- 한쪽 태그 이름을 바꾸면 다른쪽도 바뀜

### CSS Peek

- HTML에서 정의 되어 있는 CSS를 확인 할 수 있음

### Code Runner

- 파일 실행: `ctrl + alt + n`

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

### Quokka.js

Command palette에서 `Quokka.js: Start on Current File`를 선택하면 editor창에서
inline으로 결과를 보여줌

### Tabout

- 자동으로 닫히는 괄호/따옴표를 Tab키 넘어갈 수 있게 해줌

### npm Intellisense

- Node 패키지 자동완성 제공

---

### 테마

[vscodethemes.com](https://vscodethemes.com/)

다음 테마중 하나 선택

- Catppuccin for VSCode (+ Catppuccin Icons for VSCode)
- GitHub Theme
- Nord
- One Dark Pro
- Rose Pine
- tokyo-night
- Vague Theme (Windsuf)

### 폰트

[nerdfonts.com](https://www.nerdfonts.com/)에서 다운로드 후 설치

Nerd font icons, Ligature 지원

#### D2CodingLigature Nerd Font

- Naver에서 만듬, 한글 영어 특수문자간의 구별에 용이

#### JetBrainsMono Nerd Font

- 네모 반듯

#### Iosevka Nerd Font

발음: `요쎄브카`

- 세로로 길쭉

---

## 유용한 설정

Command palette에서 설정 이름을 검색해서 설정하거나
`Preference: Open User Settings (Json)`을 검색, `settings.json`에서 직접 편집 할 수 있다

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
