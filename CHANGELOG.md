# Changelog

## 2026-04-15

### System rule and prompt cleanup

#### docs/system/AI_RULE.md

* 특정 도구명인 Codex 표현을 제거하고, AI 도구 전반에 적용되는 규칙으로 문서 범위를 정리했다.
* AI 역할, 작업 기본 원칙, 협업 및 검토 원칙의 표현을 더 명확하게 다듬었다.
* `CURRENT_TASK.template.md`와 `NEXT_TASK.template.md`의 역할을 각각 현재 작업 기준과 후속 작업 관리 기준으로 구분해 설명했다.
* 구현 규칙은 공통 실행 기준만 남기고, 에이전트별 작업 취향이나 파일 관리에 가까운 항목은 제거해 문서 범위를 줄였다.
* 문서 갱신 규칙에서 `CHANGELOG.md`를 작업 종료 시 필수 갱신 흐름에서 제외하고, 저장소 변경 이력 문서로 분리해 관리하는 방향으로 정리했다.
* handoff 기준을 대화 길이가 아니라 context 소모와 작업 단위 종료 기준으로 수정했다.
* 중복되던 `지속적 개선` 섹션을 제거해 문서 구조를 간소화했다.

#### docs/system/AI_PROMPTS.md

* Handoff 공통 사용 기준과 호출 예시를 추가했다.
* `Conversation Handoff Prompt`의 사용 기준을 대화 길이가 아니라 context 소모 기준으로 정리했다.
* `Project Handoff Prompt`를 `Work Handoff Prompt`로 바꾸고, 하루 단위가 아니라 작업 종료·중단·전환 시점에 사용할 수 있도록 설명과 출력 구조를 정리했다.

#### docs/workflow

* 프로젝트 단위와 서비스 단위의 문서 사용 기준을 설명하는 `WORKFLOW_GUIDE.md`를 추가했다.
* `PROJECT_CONTEXT.template.md`를 목적, 현재 상황, 진행 방향, 미결정 사항 중심으로 정리하고, 기술 구조나 세부 작업 목록은 다른 문서로 분리했다.
* `SERVICE_OVERVIEW.template.md`를 실 사용자가 서비스를 이해하기 위한 문서로 정리하고, 해결하는 문제와 사용 흐름 중심으로 바꿨다.
* `CURRENT_TASK.template.md`를 현재 작업 범위, 포함/제외 항목, 수정 대상, 완료 기준, 검증 항목 중심으로 간소화했다.
* `NEXT_TASK.template.md`를 다음 작업 후보, 보류된 작업, 확인 사항, 우선순위를 관리하는 구조로 정리했다.
* `DECISION_LOG.template.md`에 고려한 대안과 다시 볼 조건을 추가해 의사결정 기록 기준을 보강했다.
* `ARCHITECTURE.template.md`를 프로젝트나 서비스의 기술 구조, 데이터 흐름, 실행 흐름, 의존성, 기술 부채를 정리하는 범용 템플릿으로 바꿨다.

## 2026-04-09

### Template document naming update

* 워크플로 문서들을 실사용 문서가 아닌 템플릿 문서로 명확히 구분하기 위해 `*.template.md` 형식으로 이름을 정리했다.
* `CURRENT_TASK`, `NEXT_TASK`, `PROJECT_CONTEXT`, `ARCHITECTURE`, `DECISION_LOG` 문서를 템플릿 기준으로 통일하고, `SERVICE_OVERVIEW.template.md`를 새로 추가했다.
* 일부 템플릿 문서 상단에는 이 문서가 언제, 어떻게 쓰이는지 빠르게 이해할 수 있도록 간단한 사용 안내를 덧붙였다.
* 관련 문서 참조가 깨지지 않도록 `README.md`의 구조 설명과 사용 방법도 새 파일명 기준에 맞게 함께 수정했다.

## 2026-04-07

### AI rule update

* `docs/system/AI_RULE.md`를 현재 저장소 구조와 작업 방식에 맞게 재정리했다.
* AI를 단순히 구현을 대신하는 도구로 쓰기보다, 문서를 기준으로 범위를 정리하고 작은 단위로 구현과 검증을 이어가는 작업 파트너로 사용하는 방향을 더 분명히 했다.
* 작업 범위를 먼저 정리하고, 중요한 판단과 영향 범위를 문서에 남기도록 협업 원칙을 보강했다.
* 이번 변경은 AI 활용 능력과 별개로 직접 구현과 디버깅 훈련이 약해질 수 있다는 점을 보완하기 위해 추가했다.
* 앞으로는 AI 작업 방식은 유지하되, 구현과 디버깅에서 직접 부딪히는 구간을 의식적으로 늘리는 방향을 기준으로 삼는다.
* 변경 이력을 추적할 수 있도록 `CHANGELOG.md`를 추가했다.
