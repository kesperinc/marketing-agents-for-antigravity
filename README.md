# Marketing Agents for Antigravity

이 리포지토리는 Antigravity AI를 활용하여 자율적인 **AI 마케팅 팀**을 구축하는 방법과, 여러 환경에서 Antigravity 데이터를 안전하게 관리하고 **동기화**하는 가이드를 담고 있습니다.

---

## 🚀 주요 가이드 내용

### 1. 자율 AI 마케팅 팀 구축 ([Marketing Agents.md](file:///c:/Users/MZC01-SUNKIM317/.gemini/antigravity/scratch/antigravity-guide/Marketing%20Agents.md))
최신 멀티 에이전트 프레임워크(CrewAI, AutoGen 등)의 설계 원칙을 Antigravity 환경에 맞게 통합한 가이드입니다.
- **전문 역할 분담**: CMO, 시장 조사관, 콘텐츠 전략가 등 각기 다른 목표(Goal)와 배경(Backstory)을 가진 6종의 에이전트 정의.
- **고급 워크플로우**: 순차적(Sequential) 및 계층적(Hierarchical) 협업 모델을 통한 효율적 업무 배분.
- **지속성 및 자동화**: 세션 간 맥락을 유지하는 **에이전트 메모리** 시스템과 `weekly-plan.md` 기반의 **시간 인지형 자동화** 스케줄링.
- **품질 보장**: '사람의 개입(Human-in-the-Loop)' 체크포인트를 통한 전략적 승인 및 검수 프로세스.

### 2. Antigravity 데이터 동기화 및 관리 ([ANTIGRAVITY_SYNC_GUIDE.md](file:///c:/Users/MZC01-SUNKIM317/.gemini/antigravity/scratch/antigravity-guide/ANTIGRAVITY_SYNC_GUIDE.md))
여러 대의 PC에서 Antigravity를 사용하면서 발생하는 데이터 동기화 문제를 해결하는 방법론입니다.
- **클라우드 동기화**: 심볼릭 링크(Symlink)와 OneDrive/Google Drive를 활용한 실시간 데이터 공유.
- **히스토리 병합**: 여러 기기에서 작업한 대화 기록(`conversations/`), 브레인 데이터(`brain/`), 프로젝트 소스(`scratch/`)를 수동으로 병합하는 방법.
- **플랫폼 팁**: 소형 파일 동기화에 안정적인 OneDrive 추천 및 Google Drive의 '내 드라이브' 관리 요령.

---

## 📂 리포지토리 구성
- **Marketing Agents.md**: 에이전트 팀 빌딩 및 자율 운영 핵심 가이드.
- **ANTIGRAVITY_SYNC_GUIDE.md**: 멀티 PC 환경을 위한 데이터 최적화 가이드.

---
> [!TIP]
> **Antigravity**를 처음 사용하신다면 `ANTIGRAVITY_SYNC_GUIDE.md`를 통해 환경을 먼저 설정하신 후, `Marketing Agents.md`를 참고하여 나만의 마케팅 자동화 팀을 구축해 보세요.
