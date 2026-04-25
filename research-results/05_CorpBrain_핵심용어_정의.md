# CorpBrain 핵심 기능 네이밍 가이드 (P-Reinforce 대체)

## 1. 개요 및 변경 배경
- 기존 문서에 사용된 `P-Reinforce`는 외부에서 통용되지 않는 조어이며, 기술적 원리(강화학습)와 비즈니스 목적(지식 구조화)을 직관적으로 전달하지 못하는 한계가 있습니다.
- 향후 VPS(고객·투자자 설득) 및 PRD(개발자 소통) 단계에서는 읽는 대상의 목적이 명확히 다르므로, **독자에 맞춘 투트랙(Two-Track) 용어 전략**이 필요합니다.

## 2. 타겟별 용어 정립 전략 (Two-Track Approach)

### Track A: 비즈니스/고객 지향 (VPS, 마케팅, 제안서용)
**목표**: 기술적 난해함을 줄이고, **'결과'와 '고객 가치'**를 직관적으로 전달하는 독자적 브랜드 네이밍 채택.
- **선정 기준**: 비기술 직군 대표자도 기능의 역할을 단번에 이해할 수 있는가?
- **추천 후보군**:
  1. **자율 지식 구조화 엔진 (Autonomous Knowledge Structuring Engine)**: 기능의 본질을 가장 드라이하고 명확하게 전달.
  2. **지식 가드닝 시스템 (Knowledge Gardening System)**: 에이전트가 알아서 지식을 가꾸고 다듬어준다는 비유적 표현. 사용자 경험(UX) 측면에서 매력적.
  3. **자가 진화형 위키 엔진 (Self-Evolving Wiki Engine)**: 사용자 피드백을 통해 점점 똑똑해지고 최적화된다는 지속 가능성을 강조.

### Track B: 기술/개발 지향 (PRD, 아키텍처 설계서, 엔지니어 소통용)
**목표**: 구현의 방향성과 작동 원리를 개발자에게 오해 없이 전달하는 **표준 기술 용어** 사용.
- **선정 기준**: 오개념이 발생하지 않는 명확한 아키텍처/알고리즘 용어인가?
- **추천 후보군**:
  1. **RLHF 기반 위키 최적화 엔진 (RLHF-based Wiki Optimization)**: 인간 피드백 기반 강화학습(Reinforcement Learning from Human Feedback)이라는 업계 표준 용어 사용. 가장 명확함.
  2. **RL 기반 자율 분류 에이전트 (RL-based Autonomous Classification Agent)**: 시스템의 핵심 행동인 '분류'에 초점을 맞춘 용어.
  3. **피드백 기반 지식 그래프 튜닝 (Feedback-driven Knowledge Graph Tuning)**: 문서 간의 연결성(Graph) 최적화를 구현 관점에서 표현.

## 3. 결론 및 향후 적용 방향
- **비즈니스 명칭 (VPS 적용)**: **`자율 지식 구조화 엔진 (Autonomous Knowledge Structuring Engine)`**을 메인으로 사용하되, 작동 방식을 설명할 때 '지식 가드닝(Knowledge Gardening)'이라는 비유를 보조로 활용.
- **기술 명칭 (PRD 적용)**: 모호한 조어(P-Reinforce)를 전면 폐기하고, 업계 표준에 부합하는 **`RLHF 기반 최적화 로직`** 또는 **`RL 기반 지식 분류 엔진`**으로 통일하여 명세 작성.
