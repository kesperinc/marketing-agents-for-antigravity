# 자율 AI 마케팅 팀 구축 가이드 (Antigravity 기반)

이 문서는 Claude Code와 Cowork의 사례를 바탕으로 하여, **Antigravity** 환경에서 코드 한 줄 없이 자율적으로 작동하는 AI 마케팅 팀을 구축하는 핵심 원칙과 구조를 정리합니다.

---

## 1. 핵심 철학: "프롬프트가 아닌 채용 공고를 작성하라"

AI 에이전트를 단순한 도구로 보지 않고, 특정 역할을 수행하는 실질적인 '팀원'으로 대우합니다. 각 에이전트에게는 다음 요소가 포함된 명확한 지침이 필요합니다.

- **직함 및 업무 범위**: 무엇을 담당하는가?
- **스타일 가이드**: 어떤 톤앤매너로 행동해야 하는가?
- **배경 지식**: 회사의 목표, 제품 정보, 타겟 고객은 누구인가?
- **사용 가능 도구**: Antigravity의 어떤 기능을 활용할 수 있는가? (예: `generate_image`, `browser_subagent`)
- **스케줄**: 언제 어떤 작업을 수행해야 하는가?

---

## 2. 팀 구성 (에이전트 역할)

Antigravity는 다음 5가지 주요 역할을 가진 에이전트 팀을 구성하여 운영할 수 있습니다.

1.  **CMO (Chief Marketing Officer)**: 전체 전략 수립, 일정 관리, 각 에이전트에게 업무 위임.
2.  **콘텐츠 작가 (Content Writer)**: 블로그 포스트 작성, SEO 최적화, 이미지 생성 요청.
3.  **소셜 미디어 마케터 (Social Media Marketer)**: X/SNS 포스팅, 댓글 관리, 커뮤니티(Reddit, HN 등) 대응.
4.  **성과 검토 에이전트 (Performance Reviewer)**: 마케팅 성과 데이터 분석, 인사이트 리포트 생성.
5.  **커뮤니티 관리 에이전트 (Community Manager)**: 특정 플랫폼(Hacker News 등) 특화 대응.

---

## 3. 시스템 구조 및 설정

### 📂 폴더 구조
```text
.antigravity/
├── agents/            # 각 에이전트의 역할 정의 (Markdown)
├── rules/             # 공통 규칙 (SEO, UTM, 이미지 규격 등)
└── agent-memory/      # 각 에이전트의 지속 기억 공간
docs/
├── brand/             # 브랜드 가이드, 제품 정보
├── strategy/          # GTM 전략, 주간 일정 (weekly-plan.md)
└── insights/          # 마케팅 성과 리포트
```

### 📄 주요 설정 파일
- **`CLAUDE.md` (또는 `ANTIGRAVITY.md`)**: 프로젝트의 최상위 원칙. 에이전트 팀 구조, 보안 규칙(API 키 노출 금지), 공통 도구 사용법 정의.
- **`weekly-plan.md`**: 시간대별(예: 3시간 단위) 작업 스케줄. CMO는 이 파일을 읽고 현재 시간에 해야 할 일을 결정합니다.
- **에이전트 정의 파일 (예: `content-writer.md`)**:
    - `name`, `description`, `model`, `memory: project` 등의 메타데이터 포함.
    - 단계별 작업 순서(Workflow) 명시.

---

## 4. Antigravity 맞춤 기능 활용

Antigravity의 강력한 도구들을 활용하여 기존의 복잡한 스크립트를 대체합니다.

- **`generate_image`**: 외부 API 연동 스크립트 없이 고품질 마케팅 에셋 이미지 직접 생성.
- **`browser_subagent`**: 헤드리스 브라우저 코드 작성 없이 웹 서칭, 시장 조사, SNS 포스팅 자동화.
- **`run_command`**: 필요한 경우 커스텀 Node.js/Python 스크립트(Slack 알림 등) 실행.
- **`search_web` / `read_url_content`**: 실시간 트렌드 파악 및 경쟁사 분석.

---

## 5. 피드백 루프 (자율 학습)

시스템이 멈추지 않고 발전하기 위한 순환 구조를 구축합니다.

1.  **활동 기록**: 소셜 미디어 마케터가 활동 내역을 CSV/Markdown에 기록.
2.  **분석 및 보고**: 성과 검토 에이전트가 기록을 읽고 `marketing-insights.md` 업데이트.
3.  **전략 수정**: CMO가 인사이트를 반영하여 `weekly-plan.md`나 에이전트 지침을 수정하도록 제안.
4.  **실행**: 개선된 지침에 따라 다음 콘텐츠 및 활동 수행.

---

## 6. 보안 및 모니터링 (Slack 연동)

- **`--dangerously-skip-permissions`**: Antigravity를 자율 모드로 실행할 때 사용 (감독 없이 작업 수행).
- **Slack 알림**: 각 에이전트의 활동(포스팅 완료, 오류 발생 등)을 실시간으로 Slack 채널에 보고하여 투명한 모니터링 환경 조성.
- **보안 원칙**: API 키나 민감 정보는 환경 변수로 관리하며, 에이전트가 기록에 남기지 못하도록 `rules`에 명시.

---
> [!TIP]
> **Antigravity 적용 포인트**: Antigravity의 `Implementation Plan`과 `Task` 관리 기능을 마케팅 워크플로우에 결합하면 더욱 강력한 자율 운영이 가능합니다.
