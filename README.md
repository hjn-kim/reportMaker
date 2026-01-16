# reportMaker
report_ai/
├── main.py                # 진입점 (CLI / API)
├── config/
│   ├── settings.py        # 모델, 온도, 경로
│   └── prompts.yaml       # 모든 프롬프트
├── core/
│   ├── llm_client.py      # OpenAI 호출 래퍼
│   ├── pipeline.py        # 전체 실행 흐름
│   └── state.py           # 상태 객체
├── stages/                # 보고서 단계별 로직
│   ├── planner.py
│   ├── research.py
│   ├── verifier.py
│   ├── outline.py
│   ├── writer.py
│   ├── critic.py
│   └── editor.py
├── rag/
│   ├── loader.py
│   ├── embedder.py
│   ├── vector_store.py
│   └── retriever.py
├── models/
│   ├── plan.py            # Pydantic schemas
│   ├── outline.py
│   └── critique.py
├── storage/
│   ├── db.py              # SQLite / Postgres
│   └── files.py           # 중간 결과 저장
└── utils/
    ├── retry.py
    ├── json_guard.py
    └── logger.py



    https://github.com/jh941213/STORM_Research_AG



    보고서 기본 정보

title (보고서 제목) → 최종 보고서 제목

subtitle (부제/소제목) → 필요시 추가

author (작성자 이름) → 보고서에 포함 가능

date (작성일/발행일) → 자동 생성 가능

language (언어) → 한국어, 영어 등

tone (톤) → 학술적, 친근한, 설득적 등

audience (대상 독자) → 학생, 연구자, 경영진 등

format (보고서 형식) → PDF, Markdown, HTML, LaTeX 등

보고서 구조/스타일

sections (섹션 구성) → 예: 서론, 본론, 결론

section_level (섹션 깊이) → 1~3단계

max_word_count (최대 글자/단어 수)

max_tokens (모델 사용 시 최대 토큰 수)

include_summary (요약 포함 여부) → Executive Summary

include_references (참고문헌 포함 여부)

cite_style (인용 스타일) → APA, MLA, IEEE 등

visuals (표/차트/그림 포함 여부)

highlight_keypoints (핵심 포인트 강조 여부)

내용 중점 / 연구 범위

focus_points (중점 내용) → 강조할 키워드/주제

avoid_points (제외할 내용) → 필요 없는 정보 배제

depth_level (심층 분석 수준) → 표면, 중간, 전문가 수준

perspective (관점/시각) → 경제적, 사회적, 기술적, 윤리적

bias_avoidance (편향 방지 여부) → 객관적 보고서

자료 활용 관련

source_type (자료 종류) → 학술 논문, 뉴스, 웹, 위키, 보고서, 데이터셋

rag_docs (RAG용 문서/링크) → 외부 자료 불러오기

priority_sources (우선 참고 자료) → 예: ArXiv, Naver News

exclude_sources (제외 자료)

use_latest_data (최신 자료 사용 여부)

data_format (자료 형식) → PDF, CSV, HTML, JSON 등

num_sources (참고 자료 개수 제한)

source_quality (자료 신뢰도 기준) → peer-reviewed, 공신력 뉴스 등

스타일링 / 문체

writing_style → 논문체, 보고서체, 블로그형

vocabulary_level → 초급, 중급, 전문용어 포함 여부

sentence_complexity → 단문, 복문, 전문적 문장

include_figures → 그래프/이미지 삽입 여부

citation_in_text → 본문 내 인용 방식

AI 모델/기술 관련

model → GPT-4, GPT-4o, Claude 등

temperature → 창의성/자유도 조절

max_tokens → 보고서 분량 조절

parallel_agents → 멀티에이전트 활용 여부

num_agents → 분석가 수

num_interview_turns → 질의-응답 반복 수

rag_enabled → RAG(문서 기반 답변) 사용 여부

추가 기능

feedback_mode → 피드백 기반 보고서 개선

track_changes → 보고서 히스토리/버전 관리

interactive_review → 실시간 검토/코멘트 기능

appendices → 부록/참고자료 포함 여부

summary_level → 요약/초록 길이 조절

questionnaire → 보고서 질문/응답 포함 여부

keyword_highlighting → 핵심 키워드 강조

출력 옵션

file_type → PDF, DOCX, Markdown, HTML

include_toc → 목차 포함 여부

include_page_numbers → 페이지 번호 표시

layout_style → 단락/섹션 레이아웃

export_images → 그래프/차트 별도 파일 저장



