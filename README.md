# entersq — Squad Docs

Squad 내부 프로젝트 문서(로드맵, PRD, 미팅록 등)를 보관하고 관리하는 레포지토리입니다.

## 📁 레포 구조

```
entersq/
├── README.md                 ← 이 문서 (스쿼드 인덱스)
├── _squad/                   ← 스쿼드 공통 문서 (OKR, 위클리, 정책 등)
├── _templates/               ← 새 프로젝트 시작용 템플릿
│   └── project/              ← 프로젝트 스켈레톤 (README + 기본 폴더)
├── byeol/                    ← 🌟 별(Byeol, 가칭) — AllKpop 서브 프로젝트
│   ├── README.md
│   ├── TEAM_SHARE.md
│   ├── 01_Roadmap/
│   ├── 02_PRD/
│   ├── 03_Meeting-Notes/
│   └── _archive/
└── (future projects...)
```

## 🗂 프로젝트 목록

| 프로젝트 | 상태 | 현재 버전 | 경로 |
|----------|------|-----------|------|
| 별(Byeol, 가칭) | 🟢 Active — 베타 MVP 준비 | v0.3 | [`byeol/`](./byeol) |

## 🆕 새 프로젝트 시작 가이드

1. `_templates/project/` 를 복사하여 새 프로젝트명 폴더 생성 (소문자 슬러그 권장: `project-name/`)
2. 해당 폴더 안에 `README.md`, `01_Roadmap/`, `02_PRD/`, `03_Meeting-Notes/` 구성
3. 이 README의 "프로젝트 목록" 표에 새 행 추가
4. 첫 문서 커밋 후 Slack `#ch-squad-enter` 에 업데이트 공유

## 📝 네이밍 규칙

- 프로젝트 폴더: 소문자 슬러그 (`byeol`, `project-name`)
- 문서 버전: `Roadmap_vX.Y.md`, `PRD_vX.Y.md` 형식 유지
- 최신 문서: `_vX.Y_CURRENT.md` 접미사로 현재 버전 표시
- 이전 버전: 같은 폴더에 보관 (아카이빙은 `_archive/`)

## 📢 공유 채널

- Slack: [#ch-squad-enter](https://publhq.slack.com/archives/C0AN99YRA92)
- 문서 업데이트 양식은 `byeol/TEAM_SHARE.md` 참고
