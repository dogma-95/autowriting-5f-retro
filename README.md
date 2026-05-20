# 오토라이팅 & 3F/5F 회고

머릿속에 얽힌 생각과 감정을 검열 없이 꺼내고,
**Fact / Feeling / Finding** 으로 디코딩해서 작은 다음 행동으로 연결하는 셀프코칭 시스템.

> 정리가 아니다. 외부화다. 먼저 꺼내고, 나중에 구조화한다.

이 패키지는 Claude / ChatGPT / Gemini 어느 도구에서든 30분 안에 셋업 가능하도록 만들어진 가이드와 시스템 프롬프트 모음이다.

## 빠른 시작 — 쓰는 도구를 고르세요

| 도구 | 셋업 시간 | 가이드 |
|---|---|---|
| **Claude** (Projects / 무료) | 5분 | [platforms/claude](platforms/claude/) |
| **ChatGPT** (Projects / GPTs / 무료) | 5분 | [platforms/chatgpt](platforms/chatgpt/) |
| **Gemini** (Gems / 무료) | 5분 | [platforms/gemini](platforms/gemini/) |

세 플랫폼은 강점이 달라서 시스템 프롬프트를 **각각에 맞게 재단**했다.

- **Claude**: 자연어 트리거 + Artifact로 결과물 분리 출력 (복붙해서 노션·옵시디언으로 옮기기 좋음)
- **ChatGPT**: 짧은 명령어("오토라이팅 시작", "3F 정리" 등) + 파일 업로드 워크플로우
- **Gemini**: 핵심 콘텐츠 인라인 압축 + Google Workspace(Docs / Drive / Calendar) 연동

## 한눈에 보는 제품 구조

📊 [product-map.html](docs/product-map.html) — 데일리 흐름, 운영 리듬, 시스템 컴포넌트, 3F/5F 분기, 개념 흐름, 확장 개념까지 한 페이지 시각화. 저장소에서 raw 파일을 다운로드해 브라우저로 열면 인터랙티브 다이어그램이 보입니다.

## 방법론을 먼저 읽고 싶다면

- 본문: [docs/methodology.md](docs/methodology.md)
- 감정 단어 목록: [docs/emotion-words.md](docs/emotion-words.md)
- 템플릿 모음: [docs/templates.md](docs/templates.md)
- FAQ & 운영 가이드: [docs/faq.md](docs/faq.md)

## 운영 리듬

- **평일**: 오토라이팅 후 3F 정리. 그날그날 **3F로 닫거나 5F까지 확장** 선택
  - 소화가 목적이면 3F, 전환이 목적이면 5F
  - 3F로 닫는 날을 미완료가 아니라 "소화 완료"로 봅니다
- **주말**: 한 주 기록을 모아 디코딩, 다음 주 Future Action 1~3개
- **월간**: 주간 디코딩을 모아 반복 패턴 리뷰

자세한 분기 가이드: [docs/faq.md](docs/faq.md#어떤-날은-3f만-어떤-날은-5f까지)

## 3F와 5F가 무엇인가요?

**3F (데일리 기본)**

1. **Fact** — 실제로 있었던 일, 관찰 가능한 사건. 해석/추측 분리.
2. **Feeling** — 그때 내가 느낀 감정. "힘들다"에서 한 단계 더 구체적인 단어로 라벨링.
3. **Finding** — Fact와 Feeling을 구분해보니 보이는 문제, 패턴, 통제 가능성, 가진 자원.

**5F (선택 확장)**

4. **Future Action** — 다음에 다르게 시도할 가장 작은 행동 1~3개.
5. **Feedback** — 이전 액션을 실행한 뒤 무엇이 달라졌는지.

## 패키지 구조

```
.
├── README.md                # 이 파일
├── LICENSE                  # CC BY-NC 4.0
├── docs/                    # 방법론 본문 (단일 출처)
│   ├── methodology.md
│   ├── emotion-words.md
│   ├── templates.md
│   ├── faq.md
│   └── product-map.html     # 제품 구조 시각화 (브라우저에서 열기)
├── platforms/               # 플랫폼별 셋업
│   ├── claude/
│   ├── chatgpt/
│   └── gemini/
├── prompts/                 # 짧은 명령어 9개 + 유도 진입
├── templates/               # 데일리·주말·월간 템플릿 8개
└── calendar/                # 캘린더 등록 문구
```

## 짧은 명령어 (모든 플랫폼 공통)

| 명령어 | 동작 |
|---|---|
| `오토라이팅 시작` | 시작 문장 3개 + 막혔을 때 이어갈 문장 제안 |
| `막혔어요` / `유도해줘` | 유도 모드 — AI가 한 번에 한 가지씩 질문 |
| `추론해줘` / `그냥 만들어줘` | 추론 모드 — 편린에서 AI가 3F 초안 작성 |
| `3F 정리` | 원문을 Fact / Feeling / Finding으로 분리 + 분기 질문 |
| `5F까지` | 3F를 바탕으로 Future Action + Feedback 확장 |
| `3F로 닫기` | 핵심 문장 1개 + 관찰 포인트 1개로 마무리 |
| `벽에 붙은 파리` | 제3자 시점으로 사건 재묘사 + 새 Finding |
| `1년 뒤의 나` | 미래 시점에서 무엇이 크게/작게 보일지 정리 |
| `주말 디코딩` | 한 주 기록을 9개 항목으로 디코딩 |
| `월간 리뷰` | 한 달 주간 디코딩을 8개 항목으로 리뷰 |
| `팀원 5F` | 팀원 1:1/회고용 부담 적은 안내 멘트 |

전체 프롬프트는 [prompts/](prompts/) 참고.

## 라이선스

[CC BY-NC 4.0](LICENSE) — **비상업적 용도**로 자유롭게 공유·수정·번역·변형 가능. 출처([dogma-95](https://github.com/dogma-95))를 표시해주세요.

**상업적 활용**(SaaS 통합, 유료 교육 프로그램, 출판, 회사 제품 등)을 원하시면 [GitHub 프로필](https://github.com/dogma-95)을 통해 문의 부탁드립니다.

> v1.0.0 / v1.0.1은 CC BY 4.0으로 배포되었습니다. v1.1.0부터 라이선스가 CC BY-NC 4.0으로 변경되었습니다.

## 기여

방법론 개선 제안, 다른 플랫폼(Notion / Obsidian / Logseq 등) 어댑터, 영문 번역 등 환영.
**비상업 기여**는 이슈나 PR로 의견 주세요.

## 만든 사람

[dogma-95](https://github.com/dogma-95) — 본인의 리더십 셀프코칭 흐름을 다듬어 패키지로 공유합니다.
이 방법론은 본인이 실제로 운영하며 검증한 흐름을 정리한 것입니다.
