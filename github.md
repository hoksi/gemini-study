# 학습 내용 GitHub에 저장하기

지금까지 진행한 학습 내용(`GEMINI.md`, `a01_basic` 폴더 등)을 GitHub에 저장하여 관리하면, 변경 이력을 추적하고 어디서든 접근할 수 있는 장점이 있습니다. 아래 단계에 따라 현재 프로젝트를 GitHub에 올려보세요.

### 1단계: GitHub에서 새 저장소(Repository) 만들기

1.  **GitHub 로그인**: [GitHub](https://github.com)에 로그인합니다.
2.  **새 저장소 생성**: 오른쪽 상단의 `+` 아이콘을 클릭하고 **New repository**를 선택합니다.
3.  **저장소 설정**:
    *   **Repository name**: `gemini_study`와 같이 원하는 저장소 이름을 입력합니다.
    *   **Description (optional)**: "Gemini CLI 학습 기록"과 같이 간단한 설명을 추가합니다.
    *   **Public / Private**: 저장소 공개 여부를 선택합니다. (혼자 볼 것이라면 `Private` 추천)
4.  **중요**: **`Add a README file`, `Add .gitignore`, `Choose a license` 옵션은 모두 체크하지 않은 상태로 둡니다.** 기존 프로젝트를 올릴 것이므로, 비어있는 저장소가 필요합니다.
5.  **Create repository** 버튼을 클릭하여 저장소를 생성합니다.

### 2단계: 터미널에서 Git 명령어로 프로젝트 업로드

이제 Gemini CLI를 사용하고 있는 터미널에서 다음 명령어들을 순서대로 실행합니다.

1.  **Git 초기화**
    현재 폴더를 Git이 관리하는 로컬 저장소로 만듭니다.
    ```bash
    git init
    ```

2.  **파일 추가 (Staging)**
    현재 폴더의 모든 파일과 폴더를 Git에 추가(commit 대상)하도록 지정합니다.
    ```bash
    git add .
    ```

3.  **첫 번째 커밋(Commit) 생성**
    파일들의 현재 상태를 "첫 커밋"이라는 메시지와 함께 저장합니다.
    ```bash
    git commit -m "Initial commit: Gemini CLI 학습 기본기 자료 추가"
    ```

4.  **원격 저장소 연결**
    로컬 저장소와 방금 GitHub에서 만든 원격 저장소를 연결합니다. **아래 명령어의 `YOUR_GITHUB_USERNAME`과 `YOUR_REPOSITORY_NAME` 부분을 실제 정보로 바꿔주세요.** (GitHub 저장소 페이지에서 HTTPS URL을 복사하여 붙여넣어도 됩니다.)
    ```bash
    git remote add origin https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPOSITORY_NAME.git
    ```

5.  **기본 브랜치 이름 변경 (권장)**
    최신 Git 정책에 따라 기본 브랜치 이름을 `main`으로 변경합니다.
    ```bash
    git branch -M main
    ```

6.  **GitHub로 푸시(Push)**
    로컬 저장소의 내용을 원격 저장소로 업로드합니다.
    ```bash
    git push -u origin main
    ```

이제 GitHub 저장소 페이지를 새로고침하면, `GEMINI.md` 파일과 `a01_basic` 폴더가 모두 업로드된 것을 확인할 수 있습니다.

---

**팁:** 앞으로 학습 내용이 추가될 때마다 아래 3개의 명령어만 반복 실행하면 변경사항을 계속 GitHub에 저장할 수 있습니다.

```bash
# 1. 변경된 모든 파일 추가
git add .

# 2. 변경 내용에 대한 메시지와 함께 커밋
git commit -m "학습 내용 추가: (여기에 변경 내용 요약)"

# 3. 원격 저장소에 푸시
git push
```
