# 개발 일지

이 문서는 프로젝트 전체의 진행 상황을 날짜별로 기록합니다.

---

## 2026-08-17 — 프로젝트 기록 환경 시작

### 오늘의 목표

- GitHub 저장소 생성
- 프로젝트 목적과 개발 순서 기록
- 공개 저장소 보안 기본 설정
- 개발 일지 구조 만들기
- 개인 기술 블로그 구축

### 완료한 작업

- `Katts2/boss-auction-settlement` 공개 저장소 생성
- README 확장
- `.gitignore` 추가
- `.env.example` 추가
- 프로젝트 개요 문서 추가
- 개발 일지 문서 추가
- `Katts2/dev-blog` 공개 저장소 생성
- Astro 기반 개인 기술 블로그 초기 구조 생성
- Cloudflare Pages와 GitHub 저장소 연결
- 기본 Pages 주소 `dev-blog-5jp.pages.dev` 배포
- 커스텀 도메인 `blog.mongku.org` 연결
- SSL 활성화 확인
- 첫 번째 개발 글 작성
- 두 번째 개발 글 `GitHub와 Cloudflare Pages로 개발 블로그 만들기` 작성

### 프로젝트 개발 순서

```text
0단계 개발 기록 환경
→ 1단계 보스타이머
→ 2단계 아이템 경매
→ 3단계 정산 시스템
```

각 단계는 실제 구현과 테스트가 끝난 뒤 다음 단계로 이동합니다.

### 기록 구조

```text
실제 개발
   ↓
GitHub 프로젝트 저장소
   ↓
개발 일지 원본
   ↓
개인 기술 블로그
   ↓
Reddit 진행상황 공유
```

### 블로그 구조

```text
Markdown
   ↓
GitHub dev-blog
   ↓
Cloudflare Pages
   ↓
https://blog.mongku.org
```

### 오늘 배운 내용

#### Repository

GitHub에서 하나의 프로젝트를 저장하는 공간입니다.

#### Commit

프로젝트의 변경 사항을 하나의 저장 지점으로 기록하는 것입니다.
게임의 세이브 포인트처럼 생각할 수 있습니다.

#### `.gitignore`

Git이 추적하거나 GitHub에 올리지 않아야 할 파일을 지정합니다.
이 프로젝트에서는 `.env`, 키 파일, `node_modules` 등의 파일을 제외합니다.

#### `.env.example`

실제 비밀값은 넣지 않고 프로그램이 어떤 환경변수를 필요로 하는지만 보여주는 예시 파일입니다.

#### Cloudflare Pages

GitHub 저장소의 소스를 빌드해 정적 웹사이트로 배포하는 데 사용합니다. `main` 브랜치에 변경사항이 올라가면 블로그가 자동으로 다시 배포되도록 구성했습니다.

#### Custom Domain

Cloudflare Pages 기본 주소 대신 `blog.mongku.org`를 블로그의 정식 주소로 사용합니다.

### 보안 주의사항

다음 정보는 GitHub, 블로그, Reddit에 공개하지 않습니다.

- 비밀번호
- API Key / Token
- SSH Private Key
- 실제 `.env`
- 데이터베이스 비밀번호
- Cloudflare Tunnel Token
- 기타 클라우드 인증정보

### 현재 상태

- GitHub 기록 환경: **완료**
- 개인 기술 블로그: **완료**
- Reddit 기록 환경: **다음 작업**
- 0단계 개발 기록 환경: **진행 중**
- 1단계 보스타이머: 대기
- 2단계 아이템 경매: 대기
- 3단계 정산 시스템: 대기

### 다음 작업

1. Reddit 기록 방식 준비
2. 0단계 완료 확인
3. OCI AMD 서버 확인부터 보스타이머 인프라 구축 시작

---

## 앞으로 사용할 일지 형식

새로운 작업을 할 때마다 아래 항목을 계속 추가합니다.

```text
날짜
오늘의 목표
완료한 작업
사용한 명령어
발생한 문제
원인
해결 방법
오늘 배운 내용
다음 작업
```
