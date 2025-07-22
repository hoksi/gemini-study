# Gemini CLI와 VS Code 통합

## 문제 (macOS 사용자용):
`/editor` 명령어를 사용하여 VS Code를 편집기로 설정하려고 할 때, VS Code가 시스템(macOS)에 설치되어 있음에도 불구하고 Gemini CLI가 "설치되지 않음"으로 보고하는 경우가 있습니다.

## 해결책:
이 문제는 `code` 셸 명령어가 시스템의 `PATH`에 추가되지 않아 발생합니다. 이 문제를 해결하려면 다음 단계를 따르세요:

1.  Visual Studio Code를 엽니다.
2.  명령 팔레트(`Cmd+Shift-P`)를 엽니다.
3.  `Shell Command`를 입력합니다.
4.  **`Shell Command: Install 'code' command in PATH`** 명령어를 선택하고 실행합니다.
5.  변경 사항을 적용하려면 터미널 또는 Gemini CLI를 다시 시작합니다.

이렇게 하면 `code` 명령어가 명령줄에서 접근 가능해져 Gemini CLI가 VS Code와 올바르게 통합될 수 있습니다.