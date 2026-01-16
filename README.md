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

