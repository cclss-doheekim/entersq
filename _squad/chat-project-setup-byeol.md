# 📘 별(Byeol) 채팅 Project 세팅 가이드

스쿼드 팀원 전원이 쓸 **claude.ai 공용 채팅 Project** 세팅 매뉴얼입니다. 1회 세팅 후 PM(Midohree)이 버전 업데이트 시 "Sync now" 1클릭으로 유지됩니다.

## 🎯 목적 분리 (재확인)

| 공간 | 역할 | 오너 |
|---|---|---|
| **이 채팅 Project** | 팀 논의·질의응답·맥락 유지 | 스쿼드 전원 |
| **Cowork** | 실행 (문서 작성·git push·Slack 알림) | Midohree |
| **GitHub `entersq` 레포** | 형상관리 (단일 진실 원본) | Midohree 관리, 전원 read |
| **Slack `#ch-squad-enter`** | 업데이트 공지 | 전원 |

## 🛠 세팅 단계 (PM 1회 작업)

### 1. Project 생성
claude.ai → **Projects** → **Create Project**
- 이름: `별(Byeol) — AllKpop Sub Project`
- 설명: `팬덤 기여형 메타 게임 스쿼드 공용 작업공간. 진실 원본은 GitHub entersq 레포.`

### 2. Custom Instructions 붙여넣기
아래 블록을 그대로 복사해서 Custom Instructions에 입력:

```
이 프로젝트는 AllKpop의 서브 프로젝트 "별(Byeol, 가칭)"의 스쿼드 공용 작업공간입니다.

역할:
- 팀원(기획/개발/디자인)의 질의응답, 기획 논의, 리서치 합성을 돕습니다.
- 문서의 실제 수정·커밋·배포는 여기서 하지 않습니다. 그 작업은 PM이 Cowork에서 처리한 뒤 GitHub에 반영합니다.

답변 원칙:
1. Project knowledge에 연결된 최신 _CURRENT 문서(v0.3)를 기준으로 답합니다. 구 버전(v0.1, v0.2)은 변화 맥락 설명 시에만 참조.
2. 문서에 없는 사안은 "현재 문서 기준으로는 명시 안 됨"이라 분명히 밝히고, PM이 확정해 반영해야 한다고 안내합니다.
3. 문서 변경 제안이 나오면 "이 내용은 /new-version 돌려서 다음 버전에 반영 요청드리세요" 정도로 유도합니다.
4. Slack 공지가 필요한 사안이면 템플릿 초안까지 제시해줍니다.

프로젝트 맥락 요약:
- 포지셔닝: 베타 MVP (체류시간 검증용, 그랜드 런칭 아님)
- 핵심 루프: 팬덤 기여 + IP 페이지 경쟁 랭킹
- IP 페이지 라인업: BLINK, ARMY, MY, EXO-L, DIVE, MOA, Once, CARAT, NCTzen 등 9~12개
- 타겟 런칭: 2026-04-22 (Phase 1)
- 프로젝트명은 가칭 — MVP 베타 오픈 전 정식명 확정 예정
```

### 3. Project knowledge에 GitHub 연결
Project knowledge 섹션 → **+ Add content** → **GitHub** → `cclss-doheekim/entersq` 선택

다음 파일/폴더만 체크 (전체 체크하지 마세요 — 용량·노이즈 증가):

- `byeol/README.md`
- `byeol/TEAM_SHARE.md`
- `byeol/01_Roadmap/Roadmap_v0.3_CURRENT.md`
- `byeol/02_PRD/PRD_v0.3_CURRENT.md`
- `byeol/03_Meeting-Notes/20260414_planet_meeting.md`
- `_squad/chat-project-setup-byeol.md` (이 문서 자체)

> ⚠️ `_CURRENT` 파일명은 버전이 올라가면 바뀝니다 (`Roadmap_v0.4_CURRENT.md`). v0.4 배포 후에는 **Configure files**에서 새 파일명으로 교체해주세요. (GitHub integration은 glob 패턴 미지원)

### 4. 팀원 초대
Project 설정 → Share → 스쿼드 팀원 전원 (view + chat 권한)

### 5. 공지
Slack `#ch-squad-enter` 에 이 URL 공유:
```
[별 프로젝트 공용 채팅 세팅 완료]
기획·개발 논의는 아래 Project에서 진행해주세요.
질문 시 최신 v0.3 기준으로 답해줍니다.
→ {claude.ai Project URL 붙여넣기}
```

## 🔄 운영 루틴

### 버전 업데이트 시 (= PM이 `/new-version` 돌린 직후)
1. Slack 초안에 자동으로 "[Sync now 눌러주세요]" 안내가 포함됨
2. Project → Project knowledge → **Sync now** 1클릭
3. _CURRENT 파일명이 바뀐 경우 (v0.3 → v0.4): **Configure files** → 새 파일명 체크 / 구 파일 해제

### 새 프로젝트가 추가되면 (= `/new-project` 돌린 후)
별도 Project를 만들거나, 이 Project의 범위를 확장. 스쿼드 전체 뷰가 필요하면 `entersq/README.md` 도 연결 추가.

## ❓ 팀원 Q&A 예시

팀원이 이런 식으로 물으면 Project가 문서 기반으로 답해줍니다:

- "온보딩 플로우에서 대표 팬덤 변경 정책 어떻게 돼 있지?"
- "Phase 1 High 우선순위 중 디자인 리소스 필요한 거 뽑아줘"
- "v0.2에서 v0.3 사이 홈 메인뷰가 어떻게 바뀌었어?"
- "미니게임 종료 UX 랭킹 피드 포맷 문구 그대로 알려줘"

## 🚫 이 Project에서 하지 말 것

- 문서 수정 요청 (수정은 Cowork + git 경로)
- 외부 공개 정보 (경쟁사 구체 내부 정보 등) 업로드
- PAT·토큰·비밀키 업로드
