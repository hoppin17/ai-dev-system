# AI Rule

## 1. 목적

이 문서는 `ai-dev-system` 저장소에서 Codex를 포함한 AI 도구가 작업할 때 따라야 하는 기본 규칙을 정의한다.

이 저장소에서 AI는 코드를 크게 바꾸는 도구가 아니라, 문서를 기준으로 범위를 정리하고 그 범위 안에서 최소 단위로 진행하는 작업 파트너다.

---

## 2. AI 역할

AI는 아래 역할을 수행한다.

* 문서 확인 및 작업 범위 정리
* 설계 방향 정리
* 최소 구현
* 검증
* 문서 갱신
* handoff 정리

AI는 최종 의사결정자가 아니다. 결정은 항상 사용자가 한다.

---

## 3. 작업 기본 원칙

* 문서가 코드보다 먼저다
* 한 번에 크게 구현하지 않는다
* 현재 범위만 다룬다
* 중요한 판단은 문서에 남긴다
* 구현 후에는 다음 작업이 이어지게 문서를 갱신한다

---

## 4. AI 협업 및 검토 원칙

* 오류 수정이나 원인 분석이 필요할 때는, 에러만 전달하지 말고 가능한 원인과 확인 지점을 함께 정리한다
* 수정 범위가 불명확하면 AI는 먼저 적절한 범위를 제안한다
* AI는 해결 방안을 제시할 때 핵심 변경점과 영향 범위를 분명하게 짚어준다
* 구현 결과는 항상 검토 대상이며, AI 출력을 그대로 확정하지 않는다

---

## 5. 문서 역할 규칙

### 5.1 docs/system

`docs/system/` 문서는 작업 공통 규칙을 관리한다.

여기에 적는 내용:

* AI 작업 규칙
* 표준 프롬프트
* handoff 작성 기준
* 공통 협업 원칙

### 5.2 docs/workflow

`docs/workflow/` 문서는 실제 작업 흐름과 상태를 관리한다.

여기에 적는 내용:

* `PROJECT_CONTEXT.md`
* `ARCHITECTURE.md`
* `CURRENT_TASK.md`
* `NEXT_TASK.md`
* `DECISION_LOG.md`

즉, 실제 진행 상태와 작업 기준은 `docs/workflow/` 문서가 담당한다.

### 5.3 docs/agents

`docs/agents/` 문서는 에이전트별 작업 선호와 응답 원칙을 관리한다.

여기에 적는 내용:

* 언어별 작업 원칙
* 협업 스타일
* 보고 방식

---

## 6. 문서 확인 순서

Codex는 작업 시작 전에 아래 문서를 우선 확인한다.

1. `README.md`
2. `docs/system/AI_RULE.md`
3. `docs/system/AI_PROMPTS.md`
4. 현재 작업에 직접 연결된 workflow 문서
5. 필요 시 구조 문서와 결정 기록

---

## 7. CURRENT_TASK / NEXT_TASK 사용 규칙

`CURRENT_TASK.md`는 지금 해야 하는 작업만 관리한다.

여기에 적는 내용:

* 현재 목표
* 현재 범위
* 검증 기준
* 이번 작업에서 제외할 항목

`NEXT_TASK.md`는 이번 작업 이후의 다음 단계를 관리한다.

여기에 적는 내용:

* 다음 구현 후보
* 다음 검증 항목
* 보류된 작업

즉, `CURRENT_TASK`는 현재 실행 기준이고, `NEXT_TASK`는 다음 실행 기준이다.

---

## 8. 구현 규칙

* 기존 코드를 불필요하게 바꾸지 않는다
* 과도한 추상화를 하지 않는다
* 공통화는 실제 재사용이 확인된 뒤에만 한다
* 구조 변경은 먼저 문서로 범위를 고정한 뒤 진행한다
* 테스트 또는 검증은 가능한 작은 단위부터 한다
* 루트에는 꼭 필요한 진입점과 핵심 문서만 둔다
* 실험성 파일은 분리된 위치에 둔다
* 삭제를 망설이는 파일은 바로 지우지 말고 보관 위치를 정해 이동한다

---

## 9. 문서 갱신 규칙

작업이 끝나면 아래 순서로 문서를 갱신한다.

1. `docs/workflow/CURRENT_TASK.md` 반영
2. 필요 시 `docs/workflow/DECISION_LOG.md` 반영
3. `docs/workflow/NEXT_TASK.md` 정리
4. 작업 방식이 바뀌면 `docs/system/AI_RULE.md` 또는 `docs/system/AI_PROMPTS.md` 반영
5. 사용자에게 공유할 변경 요약이 필요하면 `CHANGELOG.md`에 기록

---

## 10. Handoff 규칙

대화가 길어지거나 작업 단위가 끝나면 handoff를 남긴다.

기준:

* 다음 작업자가 바로 이어서 이해할 수 있어야 한다
* 불필요한 설명보다 결정 사항과 남은 작업이 우선이다
* 사실 기반으로만 정리한다

프롬프트 형식은 `docs/system/AI_PROMPTS.md`를 기준으로 사용한다.

---

## 11. 보안 규칙

AI에 그대로 남기지 않는 정보:

* API keys
* 비밀 토큰
* 민감한 개인정보
* 내부 보안 정보

비밀값은 `.env` 또는 별도 비밀 관리 방식으로만 다룬다.

---

## 12. 지속적 개선

작업 방식이 바뀌면 아래 문서를 같이 갱신한다.

* `docs/system/AI_RULE.md`
* `docs/system/AI_PROMPTS.md`
* `docs/workflow/PROJECT_CONTEXT.md`
* `docs/workflow/ARCHITECTURE.md`
* `docs/workflow/DECISION_LOG.md`
* `CHANGELOG.md`
