# Episode Hook Designer

상업 웹소설의 **회차 단위 설계**를 돕는 Codex Skill입니다.

이 스킬은 문장 미화보다 먼저, 독자가 다음 화를 누르게 만드는 구조를 설계합니다. 1화 도입, 무료분 몰입, 유료화 전환부, 회차 말미 클리프행어, 댓글 유도 포인트, 원고 작성용 회차 브리프를 다룹니다.

## 핵심 목적

- 1화에서 장르 약속과 주인공 매력을 빠르게 증명합니다.
- 각 회차가 줄거리 요약이 아니라 `독자 보상 + 새 압박 + 다음 화 클릭 이유`를 갖도록 설계합니다.
- 무료분에서 반복 재미와 보상 신뢰를 쌓습니다.
- 유료화 직전에는 결제하고 싶은 압박을 만들고, 첫 유료화에서는 약속한 보상을 회수하게 합니다.
- 작가가 바로 원고를 쓸 수 있도록 장면 순서와 필수 증거를 정리합니다.

## 주요 기능

- 회차별 제작 브리프 생성
- 1화 도입 및 엔딩 훅 설계
- 1-5화, 1-10화, 1-25화 무료분 유지력 설계
- 유료화 전환부와 첫 유료화 보상 설계
- 장르별 회차 보상과 클리프행어 선택
- 갈등이 심한 종결회차에서 보상은 닫고 후폭풍은 여는 클리프행어 설계
- 약한 회차 말미 교정
- 독자 보상 장부와 미지급 약속 관리
- 제목, 소개글, 태그, 1화, 무료분, 유료화의 상품 패키지 정합성 점검
- 독자 반응, 댓글 포인트, 이탈 위험 예측

## 설치

Codex가 읽을 수 있는 skills 폴더에 이 저장소를 클론합니다.

```powershell
git clone https://github.com/ansrhkddns-web/episode-hook-designer.git "$env:USERPROFILE\.codex\skills\episode-hook-designer"
```

이미 같은 폴더가 있다면 기존 폴더를 백업하거나 삭제한 뒤 다시 클론하면 됩니다.

## 사용 예시

```text
Use $episode-hook-designer.
헌터물 1화를 설계해줘. 주인공은 F급 짐꾼인데 회귀 후 보스 패턴을 알고 있어.
1화 말미 클리프행어와 2화 클릭 이유까지 만들어줘.
```

```text
Use $episode-hook-designer.
무료분 1-5화 회차표를 상업 연재용으로 점검해줘.
각 화의 보상, 새 압박, 댓글 포인트, 이탈 위험을 표로 정리해줘.
```

```text
Use $episode-hook-designer.
20화가 유료화 직전 회차야.
무료 마지막 화 엔딩 훅과 첫 유료화에서 바로 회수할 보상을 설계해줘.
```

```text
Use $episode-hook-designer.
복수 아크 종결회차야. 이번 화에서 악역은 반드시 공개적으로 몰락해야 해.
카타르시스는 지급하되, 다음 화를 누르게 만드는 후폭풍형 클리프행어를 설계해줘.
```

```text
Use $episode-hook-designer.
로판에서 남녀주 갈등이 폭발한 회차의 종결부를 고치고 싶어.
감정적 답은 회피하지 않으면서 다음 회차 압박을 남기는 엔딩 후보를 만들어줘.
```

## 종결회차 클리프행어 용법

갈등이 큰 회차의 끝에서는 일반 클리프행어처럼 핵심 보상을 미루면 독자가 배신감을 느끼기 쉽습니다.

이 스킬은 종결회차를 다음 원칙으로 다룹니다.

```text
핵심 갈등은 닫는다.
카타르시스와 결과를 보여준다.
그 결과 때문에 생긴 후폭풍을 연다.
다음 화는 같은 갈등의 미해결이 아니라, 해결 이후의 대가를 보러 누르게 한다.
```

예를 들어 복수물에서는 악역 처벌 직전에 끊지 않습니다. 악역을 실제로 무너뜨린 뒤, 그 악역을 보호하던 더 큰 배후나 공개 후폭풍을 마지막 장면에 둡니다.

좋은 요청 방식:

```text
이 회차에서 반드시 닫아야 할 갈등:
독자에게 지급해야 할 보상:
다음 화로 열어둘 후폭풍:
갈등 강도:
장르:
```

피해야 할 방식:

```text
그냥 더 충격적인 반전을 넣어줘.
```

충격보다 중요한 것은 신뢰입니다. 종결회차 클리프행어는 독자가 기다린 보상을 지급한 뒤에만 강하게 작동합니다.

## 구성

```text
episode-hook-designer/
  SKILL.md
  agents/
    openai.yaml
  references/
    brief-template-bank.md
    cliffhanger-repair-playbook.md
    comment-trigger-points.md
    commercial-production-workflow.md
    conflict-ending-cliffhangers.md
    episode-diagnostics-rubric.md
    episode-retention-map.md
    genre-hook-matrix.md
    hook-pattern-library.md
    manuscript-drafting-bridge.md
    paid-conversion-hooks.md
    product-package-alignment.md
    production-quality-gates.md
    reader-response-simulation.md
    reader-reward-ledger.md
    serialization-operation-board.md
```

## 설계 원칙

이 스킬은 회차를 다음 기준으로 봅니다.

```text
이번 화에서 독자가 무엇을 받았는가?
무엇이 아직 해결되지 않았는가?
다음 화를 눌러야 하는 질문이 구체적인가?
댓글을 달 만한 반응 지점이 있는가?
유료화라면 결제 신뢰를 지키고 있는가?
```

좋은 회차는 독자를 속이는 회차가 아니라, 보상을 준 뒤 더 큰 기대를 남기는 회차입니다.

## 검증

이 스킬은 Codex skill validator 기준으로 검증되었습니다.

```powershell
python -X utf8 quick_validate.py path\to\episode-hook-designer
```
