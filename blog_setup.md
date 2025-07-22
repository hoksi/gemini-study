# GitHub Pages와 Jekyll을 이용한 블로그 설정

GitHub와 연동하여 블로그를 운영하는 가장 일반적이고 효율적인 방법은 GitHub Pages와 정적 사이트 생성기인 Jekyll을 사용하는 것입니다. Jekyll은 GitHub Pages에서 기본적으로 지원하므로, 별도의 복잡한 설정 없이 쉽게 블로그를 만들 수 있습니다.

## 1. GitHub Pages와 Jekyll 개요

*   **GitHub Pages**: GitHub 저장소에 있는 HTML, CSS, JavaScript 파일들을 웹사이트로 호스팅해주는 GitHub의 무료 서비스입니다. `username.github.io`와 같은 주소로 블로그를 운영할 수 있습니다.
*   **Jekyll**: Markdown으로 작성된 텍스트를 정적 웹사이트(HTML, CSS, JS)로 변환해주는 Ruby 기반의 정적 사이트 생성기입니다. 블로그 게시물, 페이지, 카테고리 등을 쉽게 관리할 수 있도록 도와줍니다.

## 2. Jekyll 설치 준비 (사전 요구 사항)

Jekyll은 Ruby 기반이므로, 시스템에 Ruby와 Bundler가 설치되어 있어야 합니다. macOS의 경우 Ruby가 기본적으로 설치되어 있지만, 최신 버전을 사용하는 것이 좋습니다.

1.  **Ruby 설치 확인**: 터미널에서 다음 명령어를 실행하여 Ruby 버전을 확인합니다.
    ```bash
    ruby -v
    ```
    (만약 Ruby가 설치되어 있지 않거나 최신 버전이 아니라면, `rbenv` 또는 `rvm`과 같은 Ruby 버전 관리 도구를 사용하여 설치하는 것을 권장합니다.)

2.  **Bundler 설치**: Bundler는 Ruby 프로젝트의 의존성을 관리하는 도구입니다.
    ```bash
    gem install bundler
    ```

## 3. Jekyll 설치 및 새 블로그 생성

1.  **Jekyll 설치**: Bundler를 통해 Jekyll을 설치합니다.
    ```bash
    gem install jekyll bundler
    ```

2.  **새 Jekyll 사이트 생성**: 블로그를 만들고 싶은 디렉토리로 이동하여 다음 명령어를 실행합니다. `my-blog`는 블로그 폴더 이름이자 저장소 이름이 됩니다.
    ```bash
    jekyll new my-blog
    ```

3.  **블로그 디렉토리로 이동**: 생성된 블로그 디렉토리로 이동합니다.
    ```bash
    cd my-blog
    ```

4.  **로컬에서 블로그 실행 (테스트)**: 블로그가 제대로 생성되었는지 확인하기 위해 로컬 서버에서 실행해봅니다.
    ```bash
    bundle exec jekyll serve
    ```
    터미널에 출력되는 URL(일반적으로 `http://127.0.0.1:4000`)로 접속하여 블로그를 확인할 수 있습니다.

## 4. GitHub Pages에 블로그 배포

1.  **GitHub 저장소 생성**: GitHub에 로그인하여 새 저장소를 생성합니다. 저장소 이름은 `username.github.io` (여기서 `username`은 본인의 GitHub 사용자 이름) 형식으로 지정해야 합니다. 이렇게 해야 GitHub Pages가 자동으로 블로그를 호스팅합니다. (만약 프로젝트 페이지로 블로그를 만들고 싶다면, 저장소 이름은 자유롭게 지정하고 `gh-pages` 브랜치를 사용합니다.)

2.  **로컬 블로그를 Git 저장소로 초기화**: `my-blog` 디렉토리에서 다음 명령어를 실행합니다.
    ```bash
    git init
    git add .
    git commit -m "Initial Jekyll blog commit"
    ```

3.  **원격 저장소 연결**: GitHub에서 생성한 저장소의 URL을 로컬 저장소에 연결합니다.
    ```bash
    git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git
    # 또는 SSH 방식: git remote add origin git@github.com:YOUR_USERNAME/YOUR_USERNAME.github.io.git
    ```

4.  **기본 브랜치 설정**: `main` 브랜치로 설정합니다.
    ```bash
    git branch -M main
    ```

5.  **GitHub로 푸시**: 로컬 블로그 파일을 GitHub 저장소로 푸시합니다.
    ```bash
    git push -u origin main
    ```

6.  **배포 확인**: 푸시 후 몇 분 정도 기다리면 `https://YOUR_USERNAME.github.io` 주소에서 블로그가 배포된 것을 확인할 수 있습니다.

## 5. 블로그 게시물 작성

새로운 게시물은 `_posts` 디렉토리에 `YYYY-MM-DD-제목.md` 형식의 Markdown 파일로 작성합니다. 각 게시물 파일의 상단에는 YAML Front Matter를 포함해야 합니다.

**예시: `_posts/2025-07-23-my-first-post.md`**

```markdown
---
layout: post
title: "나의 첫 번째 블로그 게시물"
date: 2025-07-23 10:00:00 +0900
categories: [jekyll, blog]
---

안녕하세요! 이것은 Jekyll을 이용한 저의 첫 번째 블로그 게시물입니다.

## Markdown 사용 예시

*   항목 1
*   항목 2

```python
print("Hello, Jekyll!")
```

더 많은 내용을 여기에 작성할 수 있습니다.
```

게시물을 작성한 후에는 `git add .`, `git commit -m "새 게시물 추가"`, `git push` 명령어를 사용하여 GitHub에 푸시하면 자동으로 블로그에 반영됩니다.

---

이 가이드를 통해 자신만의 GitHub Pages 블로그를 성공적으로 설정하고 운영하시길 바랍니다.
