# Boss Timer · Item Auction · Settlement System

게임 길드/그룹을 위한 **보스타이머 → 아이템 경매 → 정산** 시스템을 단계적으로 구축하는 프로젝트입니다.

이 프로젝트는 개발 초보자가 직접 구축하고 운영하는 과정을 기록하며, 가능한 한 **Always Free / Free Tier** 인프라를 활용하는 것을 목표로 합니다.

## 개발 원칙

1. 보스타이머를 먼저 완성합니다.
2. 보스타이머가 실제 환경에서 정상 동작하고 테스트가 끝난 뒤 아이템 경매 단계로 넘어갑니다.
3. 아이템 경매가 완료된 뒤 정산 시스템을 구현합니다.
4. 한 단계가 완료되기 전에는 다음 핵심 기능을 동시에 개발하지 않습니다.
5. 비밀번호, API Key, SSH Private Key, `.env` 등 비밀정보는 GitHub에 올리지 않습니다.

## 개발 단계

| 단계 | 기능 | 상태 |
|---|---|---|
| 0 | 개발 기록 환경 구축 | 진행 중 |
| 1 | 보스타이머 | 대기 |
| 2 | 아이템 경매 | 대기 |
| 3 | 정산 시스템 | 대기 |

## 보유 / 활용 예정 인프라

- Cloudflare: 도메인, DNS 및 무료 플랜 기능
- OCI: AMD Compute 2대, OCI DB 2개
- GCP: Compute Instance 1대
- Supabase
- Firebase
- MongoDB
- Neon
- AWS Free Tier
- Azure Free Tier

> 모든 서비스를 처음부터 억지로 연결하지 않습니다. 각 단계에서 필요한 서비스만 역할을 정해서 추가합니다.

## 목표 구조

```text
Boss Timer
    ↓
보스 참여/처치 기록
    ↓
Item Auction
    ↓
낙찰 및 판매 기록
    ↓
Settlement
    ↓
개인별 정산 내역
```

## 문서

- [프로젝트 개요](docs/00-project-overview.md)
- [개발 일지](docs/01-development-log.md)

## 보안

다음 정보는 저장소에 커밋하지 않습니다.

- `.env`
- 데이터베이스 비밀번호 및 실제 Connection String
- API Key / API Token
- JWT Secret
- SSH Private Key
- Cloudflare Tunnel Token
- 각 클라우드 서비스의 인증정보

공유가 필요한 환경변수 이름은 실제 값 대신 `.env.example`에 예시만 기록합니다.

## 현재 작업

현재는 **0단계: 개발 기록 환경 구축**을 진행하고 있습니다. GitHub 기록 환경을 정리한 뒤 개인 블로그와 Reddit 기록 방식까지 준비하고, 그 다음 OCI 기반 보스타이머 구축을 시작합니다.
