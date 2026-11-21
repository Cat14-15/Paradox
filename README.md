# Paradox Base

PARALLAX 팀 유니티 프로젝트의 **초기 세팅 뼈대**입니다. 게임 내용은 들어 있지 않습니다.

## 들어 있는 것
- Unity **6000.5.0f1** 프로젝트 설정(`ProjectSettings/`)
- 패키지 목록(`Packages/manifest.json`): URP 2D, Input System, 2D 도구, Test Framework 등
- URP 2D 렌더링 설정(`Assets/Settings/`), 기본 입력 액션(`Assets/InputSystem_Actions.inputactions`)
- 빈 씬 하나(`Assets/Scenes/Main.unity`, 빌드 목록에 등록됨)
- 폴더 틀: `Assets/Scripts`, `Assets/Art`, `Assets/Audio`, `Assets/Prefabs`
- `.gitignore`(Library·Temp·Logs 등 제외), `.gitattributes`(그림·소리는 Git LFS)

## 시작하기
1. Git LFS 설치: `git lfs install`
2. 저장소 받기: `git clone https://github.com/Cat14-15/Paradox-Base.git`
3. Unity Hub → Add → 받은 폴더 선택 → Unity **6000.5.0f1**로 열기
4. `Assets/Scenes/Main.unity`를 열고 ▶ 재생

## 같이 작업하는 규칙
- **main 에 바로 올리지 않습니다.** 각자 브랜치를 만들어 작업하고 Pull Request로 합칩니다.
  ```
  git switch -c 내이름/작업이름
  git add -A
  git commit -m "무엇을 했는지"
  git push -u origin 내이름/작업이름
  ```
- **같은 씬(.unity) · 프리팹을 동시에 고치지 않습니다.** 유니티 씬은 합치기가 매우 어렵습니다. 누가 어느 씬을 맡을지 먼저 정하세요.
- 작업을 시작하기 전에 `git pull`, 끝나면 바로 커밋 · 푸시합니다.
- `Library/`, `Temp/`, `Logs/`, `UserSettings/`는 올리지 않습니다(이미 `.gitignore`에 있음).
- `.meta` 파일은 꼭 함께 올립니다(빠지면 연결이 끊깁니다).
