# FZF

[CLI Fuzzy finder](https://github.com/junegunn/fzf)

터미널에서 현재 경로 아래에 다른 경로와 파일을 검색하여 값을 반환하거나
바로 이동 또는 과거에 사용한 명령어를 검색 할 수 있다.

---

## 목록

- [준비](#준비)
- [설치](#설치)
- [설정](#설정)
- [사용](#사용)
  - [경로 또는 파일 검색](#경로-또는-파일-검색)
  - [명령어 기록 검색](#명령어-기록-검색)
  - [경로 이동](#경로-이동)

---

## 준비

- `bat`: cat의 대체. 파일을 더 괜찮은 형식으로 출력
- `eza`: ls의 대체. 아이콘, git 상태 표시 기능
- `fd-find`: find의 대체. 더 빠르고 직관적인 검색 도구

```sh
sudo apt update && sudo apt install bat eza fd-find git
```

---

## 설치

git을 이용해서 클론:

```sh
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
```

설치 스크립트 실행:

```sh
~/.fzf/install
```

프롬프트에서 전부 `y` 또는 `Enter` 입력

`~/.fzf.bash` 파일이 있으면 불러오는 스크립트가 `~/.bashrc`에 추가된다

```sh
[ -f ~/.fzf.bash ] && source ~/.fzf.bash
```

---

## 설정

VSCode로 `.bashrc` 파일을 열고

```sh
code ~/.bashrc # or ~/.zshrc
```

다음 스크립트를 추가

- `fd`: 경로와 파일을 검색
- `eza`: 경로 미리보기
- `bat`: 파일 미리보기

```sh
# fd(fdfind) instead of find for better performance
# strip away dir prefix
# do not show .git dir
export FZF_DEFAULT_COMMAND='fdfind --hidden --strip-cwd-prefix --exclude .git'
# Preview directories with eza, files with bat(batcat).
preview='if [ -d {} ]; then eza --tree --color=always {} | head -200; else batcat -n --color=always --line-range :500 {}; fi'
export FZF_CTRL_T_COMMAND="$FZF_DEFAULT_COMMAND"
export FZF_CTRL_T_OPTS="--preview '$preview'"

export FZF_ALT_C_COMMAND='fdfind --type=d --hidden --strip-cwd-prefix --exclude .git'
export FZF_ALT_C_OPTS="--preview 'eza --tree --color=always {} | head -200'"
```

저장하고 서현재 Shell(터미널)에 적용:

```sh
source ~/.bashrc # 또는 source 대신 .(온점)
```

---

## 사용

### 경로 또는 파일 검색

터미널에서 프로그램 이름 입력 후 `Ctrl + T`를 누른다:

```sh
code <Ctrl+T>
```

- 현재 경로 아래의 경로, 파일을 검색
- `Ctrl + J/K`: 아래/위 이동(또는 화살표)
- `Enter`로 선택

다음 처럼 완성된다:

```sh
code roscamp-repo-3/TechnicalResearch/server/
```

다시 `Enter`를 누르면 `VSCode`를 이용해서 해당 경로를 열게 된다

---

### 명령어 기록 검색

`Ctrl + R`

- `~/.bash_history`에서 명령어 검색 하여 사용 가능

---

### 경로 이동

`Alt + C`

- 단축키를 누른 경로 밑에 있는 경로만 검색
- 선택한 경로로 바로 이동
- `ESC` 누른 후 `c`를 눌러도 똑같이 동작
