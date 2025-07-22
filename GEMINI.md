# Gemini CLI Notes

## VS Code Integration

**Problem:**
When trying to set VS Code as the editor using the `/editor` command, Gemini CLI reports that it is "not installed", even though VS Code is installed on the system (macOS).

**Solution:**
This issue occurs when the `code` shell command is not added to the system's `PATH`. To fix this:

1.  Open Visual Studio Code.
2.  Open the Command Palette (`Cmd+Shift+P`).
3.  Type `Shell Command`.
4.  Select and run the command: **`Shell Command: Install 'code' command in PATH`**.
5.  Restart the terminal or Gemini CLI for the changes to take effect.

This ensures that the `code` command is accessible from the command line, allowing Gemini CLI to integrate with it properly.

---

## Gemini CLI 학습 계획

### 1. 기본기 다지기 (완료)

`a01_basic` 폴더에 다음 학습 자료 생성을 완료했습니다.

*   `a01_01.md`: 설치 및 인증
*   `a01_02.md`: 기본 명령어 숙달
*   `a01_03.md`: 기본 명령어 활용 사례
*   `a01_04.md`: 코드 관련 기능

### 2. 심화 학습

*   **프로젝트 맞춤설정 (`GEMINI.md`):**
    *   프로젝트 루트에 `GEMINI.md` 파일을 생성하여 AI의 응답 스타일, 규칙, 도구 사용 등을 프로젝트에 맞게 조정하는 방법 학습.
*   **멀티모달 기능 활용:**
    *   스케치나 PDF 같은 시각 자료를 기반으로 코드(HTML/CSS 등)를 생성하는 기능 실습.
*   **Model Context Protocol (MCP) 확장:**
    *   MCP 서버를 구성하여 Gemini CLI의 기능을 확장하고, 특정 API나 커스텀 모델과 연동하는 방법 학습.

### 3. 실전 적용 및 자동화

*   **워크플로우 자동화:**
    *   CI/CD 파이프라인에 Gemini CLI를 통합하여 코드 리뷰, 문서 생성 등의 작업을 자동화하는 방법 모색.
*   **체크포인팅:**
    *   파일 수정 전 자동으로 프로젝트 상태를 저장하는 체크포인팅 기능을 활성화하여 안전하게 AI 도구를 사용하는 방법 익히기.

### 참고 자료

*   **공식 문서:** Gemini CLI Documentation Hub
*   **튜토리얼 영상:** YouTube 등
*   **커뮤니티:** DataCamp, DEV Community 등