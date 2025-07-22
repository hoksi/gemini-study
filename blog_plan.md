# 블로그 생성 계획 (GitHub Pages + Jekyll)

이 계획은 GitHub Pages와 Jekyll을 사용하여 개인 블로그를 설정하는 단계를 안내합니다.

## 1단계: Jekyll 환경 설정 (완료)

Homebrew, `rbenv`, Ruby, Bundler, Jekyll 설치를 완료했습니다.

## 2단계: 새 Jekyll 블로그 생성

*   **블로그 생성**: `jekyll new YOUR_BLOG_NAME` 명령어를 사용하여 새 블로그 프로젝트를 생성합니다.
*   **로컬 테스트**: `bundle exec jekyll serve` 명령어로 블로그가 로컬에서 잘 작동하는지 확인합니다.

## 3단계: GitHub Pages에 배포

*   **GitHub 저장소 생성**: `YOUR_GITHUB_USERNAME.github.io` 형식의 새 GitHub 저장소를 생성합니다. (여기서 `YOUR_GITHUB_USERNAME`은 실제 GitHub 사용자 이름이어야 합니다.)
*   **Git 초기화 및 커밋**: 생성된 블로그 프로젝트를 Git 저장소로 초기화하고, 모든 파일을 추가 및 커밋합니다.
*   **원격 저장소 연결**: 로컬 저장소를 GitHub의 원격 저장소에 연결합니다.
*   **GitHub로 푸시**: `main` 브랜치로 푸시하여 GitHub Pages에 블로그를 배포합니다.

## 4단계: 첫 게시물 작성 및 배포

*   **게시물 작성**: `_posts` 디렉토리에 Markdown 형식으로 첫 블로그 게시물을 작성합니다.
*   **커밋 및 푸시**: 작성된 게시물을 커밋하고 GitHub에 푸시하여 블로그에 반영합니다.

---

**진행 시 필요한 정보:**

*   **GitHub 사용자 이름**: `YOUR_GITHUB_USERNAME` 대신 사용될 실제 GitHub 사용자 이름이 필요합니다.
