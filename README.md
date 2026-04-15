# AI Dev System

> AI와 함께 개발할 때 작업 범위, 문서, 구현, 검토 흐름을 일관되게 관리하기 위한 문서 기반 개발 시스템이다.

---

## Overview

이 저장소는 AI를 개발 파트너로 사용할 때 필요한 공통 작업 기준을 정리한다.

핵심 목적은 AI에게 구현을 통째로 맡기는 것이 아니라, 문서를 기준으로 범위를 먼저 정리하고 작은 단위로 구현과 검토를 이어가는 것이다.

이 저장소는 다음 문서를 포함한다.

- AI 작업 규칙
- 표준 프롬프트
- workflow 문서 템플릿
- 프로젝트 / 서비스 단위 문서 사용 가이드
- 에이전트 작업 선호 문서

---

## Goal

AI 기반 개발에서 자주 생기는 문제를 줄이는 것이 목표다.

- context가 끊겨 작업 흐름이 사라지는 문제
- 설계 없이 바로 구현하면서 범위가 커지는 문제
- 반복해서 같은 설명을 해야 하는 문제
- 결정 이유가 남지 않아 나중에 다시 판단해야 하는 문제
- 현재 작업과 다음 작업이 섞이는 문제

이를 해결하기 위해 문서를 먼저 정리하고, 그 문서 안에서 작은 작업 단위로 진행한다.

---

## Core Flow

기본 흐름은 아래와 같다.

1. 목적과 현재 상황을 정리한다.
2. 이번 작업 범위를 정한다.
3. 필요한 만큼만 설계와 구조를 확인한다.
4. 작은 단위로 쪼개서 구현한다.
5. 검증한다.
6. 결정 사항과 다음 작업을 문서에 남긴다.

간단한 작업에서는 일부 단계를 줄일 수 있다. 중요한 것은 모든 문서를 매번 채우는 것이 아니라, 현재 작업에 필요한 판단 기준을 남기는 것이다.

---

## System Structure

```text
docs/
  system/
    AI_RULE.md
    AI_PROMPTS.md

  workflow/
    WORKFLOW_GUIDE.md
    PROJECT_CONTEXT.template.md
    SERVICE_OVERVIEW.template.md
    CURRENT_TASK.template.md
    NEXT_TASK.template.md
    ARCHITECTURE.template.md
    DECISION_LOG.template.md

  agents/
    AGENTS_KR.md
    AGENTS_EN.md
```

---

## Document Roles

### docs/system/AI_RULE.md

AI 도구가 작업할 때 따라야 하는 기본 규칙을 정리한다.

- AI 역할
- 작업 기본 원칙
- 문서 확인 순서
- 구현 규칙
- 문서 갱신 규칙
- handoff 기준

### docs/system/AI_PROMPTS.md

반복해서 사용하는 표준 프롬프트를 정리한다.

- Conversation Handoff
- Work Handoff

### docs/workflow/WORKFLOW_GUIDE.md

workflow 문서를 프로젝트 단위와 서비스 단위에서 어떻게 나눠 쓰는지 설명한다.

프로젝트가 커지거나 서비스가 여러 개로 나뉠 때는 이 문서를 먼저 보고 어떤 문서를 사용할지 정한다.

### docs/workflow/PROJECT_CONTEXT.template.md

프로젝트 또는 서비스의 목적, 현재 상황, 진행 방향을 정리하는 템플릿이다.

현재 무엇을 위해 진행 중이고, 어디로 가려는지 이해하기 위한 문서다.

### docs/workflow/SERVICE_OVERVIEW.template.md

서비스가 무엇을 제공하는지 빠르게 이해하기 위한 템플릿이다.

개발자뿐 아니라 비개발자도 이해할 수 있도록, 해결하는 문제와 사용 흐름을 중심으로 정리한다.

### docs/workflow/CURRENT_TASK.template.md

현재 진행 중인 하나의 작업 범위를 정리하는 템플릿이다.

이번 작업에서 무엇을 하고, 무엇을 하지 않으며, 어떤 기준으로 완료할지를 고정한다.

### docs/workflow/NEXT_TASK.template.md

앞으로 `CURRENT_TASK`로 내려서 처리할 작업 후보를 정리하는 템플릿이다.

다음 작업 후보, 보류된 작업, 확인이 필요한 사항, 우선순위를 관리한다.

### docs/workflow/ARCHITECTURE.template.md

프로젝트 또는 서비스의 기술 구조와 흐름을 정리하는 선택 템플릿이다.

작은 서비스에서는 생략할 수 있고, 모듈이나 데이터 흐름이 복잡해질 때 추가한다.

### docs/workflow/DECISION_LOG.template.md

중요한 의사결정을 기록하는 템플릿이다.

무엇을 결정했는지보다, 왜 그렇게 결정했는지와 어떤 영향이 있는지를 남긴다.

### docs/agents/AGENTS_KR.md

특정 AI 에이전트에 종속되지 않는 개인 작업 선호와 협업 방식을 정리한 한글 버전이다.

AI가 어떤 도구나 환경에서 실행되더라도, 사용자가 선호하는 작업 방향, 설명 방식, 의사결정 흐름을 일관되게 따르도록 돕는다.

### docs/agents/AGENTS_EN.md

특정 AI 에이전트에 종속되지 않는 개인 작업 선호와 협업 방식을 정리한 영어 버전이다.

AI가 어떤 도구나 환경에서 실행되더라도, 사용자가 선호하는 작업 방향, 설명 방식, 의사결정 흐름을 일관되게 따르도록 돕는다.

---

## How To Use

### 1. 새 프로젝트에 적용할 때

1. 이 저장소의 `docs/` 구조를 새 프로젝트에 복사한다.
2. `docs/workflow/WORKFLOW_GUIDE.md`를 보고 필요한 문서를 고른다.
3. `*.template.md` 파일을 실제 문서 이름으로 복사한다.
4. 기본 문서인 `PROJECT_CONTEXT.md`, `SERVICE_OVERVIEW.md`, `DECISION_LOG.md`를 만든다.
5. `PROJECT_CONTEXT.md`에 프로젝트 또는 서비스의 목적, 현재 상황, 진행 방향을 정리한다.
6. `SERVICE_OVERVIEW.md`에 서비스가 해결하는 문제와 사용 흐름을 정리한다.
7. `DECISION_LOG.md`는 프로젝트 단위 결정 기록 문서로 유지하고, 프로젝트 전체에 영향을 주는 중요한 결정이 생길 때 기록한다.
8. 작업 범위가 커지면 `CURRENT_TASK.md`, `NEXT_TASK.md`를 추가한다.
9. 해당 프로젝트에 적용할 기술들을 정리해서 `ARCHITECTURE.md`를 추가한다.

### 2. 작은 서비스에서 시작할 때

처음부터 모든 workflow 문서를 만들 필요는 없다. 다만 기본 문서 3개는 먼저 만든다.

기본 작성 문서:

- `PROJECT_CONTEXT.md`
- `SERVICE_OVERVIEW.md`
- `DECISION_LOG.md`

작업 범위가 커지면 추가:

- `CURRENT_TASK.md`
- `NEXT_TASK.md`

기술 구조가 복잡해지면 추가:

- `ARCHITECTURE.md`

`DECISION_LOG.md`는 프로젝트 단위로 관리한다. 처음부터 문서는 만들어두고, 프로젝트 전체 방향이나 여러 서비스에 영향을 주는 중요한 결정이 생길 때 기록한다.

---

## Design Principles

- 문서가 코드보다 먼저다.
- 한 번에 하나의 범위만 작업한다.
- 필요한 변경만 한다.
- 중요한 판단은 문서에 남긴다.
- 현재 작업과 다음 작업을 분리한다.
- 작은 서비스는 최소 문서로 시작한다.
- 구조가 복잡해질 때만 문서를 추가한다.
- AI의 출력은 검토 대상이며, 최종 결정은 사용자가 한다.

---

## Anti-Patterns

- 설계 없이 바로 구현하기
- AI에게 전체 판단을 맡기기
- 모든 내용을 한 문서에 몰아넣기
- 작은 작업에 과한 문서 구조 만들기
- 현재 작업과 다음 작업을 섞기
- 결정 이유를 남기지 않기
- 실제로 바뀐 내용이 없는데 모든 문서를 갱신하기

---

## Expected Benefits

- 작업 흐름 유지
- context 단절 감소
- 반복 설명 비용 감소
- 구현 범위 관리
- 결정 기록 유지
- AI 협업 품질 향상

---

## Future Extensions

- 프로젝트 초기화 템플릿
- workflow 문서 생성 자동화
- handoff 생성 자동화
- AI 기반 문서 검토
- CLI 도구화

---

## Author

AI-assisted development system designed for practical solo and small-team development.
