
# Project road map

## 1. 프로젝트 준비 & 환경 세팅 -> Done!
- **요구사항 정리**  
  - Daily / Weekly / Monthly 리포트 기능 정의  
  - 대상 Obsidian vault 경로, 출력 포맷(PDF, Markdown) 확정  
- **레포지토리 및 툴체인 구성**  
  - `pyproject.toml` + Poetry 세팅  
  - `pre-commit`(black, isort, flake8) 구성 
  - `.env` / `config.yaml` 샘플 작성  
- **폴더 구조 뼈대 작성** 
```
obs_report/  
├── src/obs_report/  
│ ├── watcher.py  
│ ├── parser.py  
│ ├── llm_client.py  
│ ├── writer.py  
│ ├── scheduler.py  
│ └── cli.py  
├── tests/  
├── docs/  
└── pyproject.tom
```

## 2. 코어 기능 개발 -> Done!
1. **파일 감지 모듈** (`watcher.py`)  
 - glob + mtime 검사로 24h 변경 파일 리스트 반환  
 - 유닛 테스트 작성  
1. **Markdown 파서** (`parser.py`)  
 - 제목/헤더/본문/메타태그 추출 (`frontmatter`, `markdown` 라이브러리 활용)  
 - 유닛 테스트 작성  
3. **LLM 요약 클라이언트** (`llm_client.py`)  
 - Ollama REST 호출 래퍼  
 - 요청·응답 스키마 (`pydantic`) 정의  
 - Mock 테스트 작성  
4. **리포트 작성기** (`writer.py`)  
 - Daily / Weekly / Monthly Note 업데이트 로직  
 - 기존 섹션 지우고 새로 쓰기  
 - 임시 Vault에 쓰기 후 결과 검증 테스트

## 3. CLI & 스케줄러 연동 -> Done!
- **Typer 기반 CLI** (`cli.py`)  
- `run-daily`, `run-weekly`, `run-monthly` 커맨드  
- **스케줄러 스크립트** (`scheduler.py`)  
- cron 엔트리 생성 함수 (`--install-cron`)  
- Windows Task Scheduler 등록 스크립트 (Optional)  
- **통합 테스트**  
- CI 환경에서 직접 호출 후 결과 확인

## 4. 패키징 & 배포 -> Done!
- **PyInstaller**로 standalone 실행 파일 생성  
- **배포 스크립트** (`make package` or `poetry build`)  
- **설치 가이드** 및 **README** 문서화



이제 배포까지 전부 완료했습니다. 앞으로 변경사항은 없을 것 같아요