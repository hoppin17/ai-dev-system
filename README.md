# AI Dev System

> AI 기반 개발을 위한 구조화된 작업 시스템 (Plan-driven Development Framework)

---

## 📌 Overview

이 저장소는 GPT, Cursor 등의 AI 도구를 활용하여  
**일관된 방식으로 개발을 수행하기 위한 시스템**을 정의한다.

단순한 코드 저장소가 아니라 다음을 포함한다:

- 개발 규칙 (Rules)
- 표준 프롬프트 (Prompts)
- 작업 관리 템플릿 (Tasks)
- 설계 문서 구조 (Architecture)
- 의사결정 기록 (Decision Log)

---

## 🎯 Goal

AI를 활용한 개발에서 발생하는 문제를 해결하는 것이 목적이다:

- 컨텍스트 단절 문제
- 일관성 없는 작업 방식
- 설계 없이 바로 구현하는 문제
- 반복되는 설명 비용

👉 이를 해결하기 위해  
**Plan-driven 개발 방식**을 적용한다.

이 시스템은 AI를 빠르게 구현만 하는 도구로 쓰기보다,
문서를 기준으로 범위를 먼저 정리하고 작은 단위로 구현하며,
검토와 기록을 통해 다음 작업으로 이어지게 만드는 것을 목표로 한다.

AI는 결정을 대신하는 존재가 아니라,
설계, 구현, 검증, 문서 갱신을 함께 돕는 작업 파트너로 사용한다.

---

## 🧠 Core Concept

### Plan → Build → Review

모든 작업은 다음 흐름을 따른다:

1. 문제 정의
2. 설계
3. 작업 명세 작성
4. 구현
5. 리뷰

** 간단한 작업일시 일부 생략하고 진행하기도 한다

---

## 🧩 System Structure

```text
/docs
  /system
    AI_RULE.md
    AI_PROMPTS.md
  /workflow
    PROJECT_CONTEXT.md
    ARCHITECTURE.md
    CURRENT_TASK.md
    NEXT_TASK.md
    DECISION_LOG.md
  /agents
    AGENTS_KR.md
    AGENTS_EN.md
```


---

## 📄 Document Roles

### 🔹 docs/system/AI_RULE.md
AI와 협업할 때의 기본 규칙 정의

- AI 별 역할 분리
- 작업 절차 (Workflow)
- 코드 작성 규칙
- 문서화 원칙

---

### 🔹 docs/system/AI_PROMPTS.md
반복적으로 사용하는 프롬프트 템플릿

- Conversation Handoff
- Project Handoff

---

### 🔹 docs/workflow/PROJECT_CONTEXT.md
현재 프로젝트 상태와 방향 정의

👉 "지금 어디까지 왔는가"

---

### 🔹 docs/workflow/ARCHITECTURE.md
시스템 구조 설계 문서

👉 "어떻게 구성되어 있는가"

---

### 🔹 docs/workflow/CURRENT_TASK.md
현재 작업 명세

👉 "지금 무엇을 해야 하는가"

---

### 🔹 docs/workflow/NEXT_TASK.md
다음 작업 방향

👉 "다음에는 무엇을 할 것인가"

---

### 🔹 docs/workflow/DECISION_LOG.md
의사결정 기록

👉 "왜 이렇게 만들었는가"

---

## ⚙️ Workflow

1️⃣ PROJECT_CONTEXT 확인  
2️⃣ ARCHITECTURE 확인  
3️⃣ CURRENT_TASK 작성  
4️⃣ 구현  
5️⃣ 리뷰  
6️⃣ DECISION_LOG 기록  
7️⃣ NEXT_TASK 정의  

---

## 🤖 Agent Preferences

### 🔹 docs/agents/AGENTS_KR.md
개인 작업 원칙의 한글 버전

### 🔹 docs/agents/AGENTS_EN.md
개인 작업 원칙의 영어 압축본

---

## 🔥 Design Principles

- 단순성 우선 (Keep it simple)
- 계획 기반 개발 (Plan-driven)
- 문서 기반 작업 (Documentation-first)
- 범위를 먼저 고정한 뒤 구현
- 한 번에 크게 바꾸지 않기
- 중요한 판단은 문서에 남기기
- 구현 후 다음 작업이 이어지도록 문서 갱신
- 프로젝트 독립성 유지
- 불필요한 추상화 금지

---

## 🚫 Anti-Patterns

- 설계 없이 바로 코딩
- AI에게 전체를 맡기는 것
- 과도한 추상화
- 문서 없이 구조 변경

---

## 🚀 Usage

1. 이 레포를 clone
2. 새로운 프로젝트에 `/docs` 구조 복사
3. `docs/workflow/PROJECT_CONTEXT.md`부터 작성
4. `docs/workflow/CURRENT_TASK.md` 기준으로 작업 진행

---

## 📈 Expected Benefits

- 개발 속도 향상
- 작업 일관성 확보
- 컨텍스트 유지
- 리팩토링 용이성 증가
- AI 협업 효율 극대화

---

## 🧩 Future Extensions

- CLI 자동화 도구
- Task 생성 자동화
- AI 기반 코드 리뷰 자동화
- 프로젝트 템플릿화

---

## 👤 Author

AI-assisted development system designed for high-efficiency solo development.
