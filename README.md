# chatgpt-clone

OpenAI Agents SDK와 Streamlit을 사용해 ChatGPT와 유사한 채팅 앱을 만드는 프로젝트입니다.

## 현재 상태

- OpenAI Agents SDK 기반 에이전트 프로토타입 (`dummy-agent.ipynb`)
- 커스텀 도구(`function_tool`) 호출
- 스트리밍 응답(`Runner.run_streamed`) 실험
- Streamlit UI는 추후 연동 예정

## 기술 스택

- Python 3.13+
- [uv](https://github.com/astral-sh/uv) — 패키지/환경 관리
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) (`openai-agents`)
- Streamlit — 웹 UI (예정)

## 시작하기

### 1. 의존성 설치

```bash
uv sync
```

### 2. 환경 변수 설정

프로젝트 루트에 `.env` 파일을 만들고 OpenAI API 키를 추가합니다.

```env
OPENAI_API_KEY=sk-...
```

### 3. 에이전트 노트북 실행

`dummy-agent.ipynb`를 열고 커널을 `.venv`로 선택한 뒤 셀을 실행합니다.

```bash
# Jupyter 커널 등록 (최초 1회)
uv run python -m ipykernel install --user --name=chatgpt-clone --display-name="chatgpt-clone (.venv)"
```

## 프로젝트 구조

```
chatgpt-clone/
├── dummy-agent.ipynb   # 에이전트 + 도구 + 스트리밍 실험
├── main.py             # Streamlit 앱 진입점 (작성 예정)
├── pyproject.toml
└── uv.lock
```

## 로드맵

- [ ] Streamlit 채팅 UI 구현
- [ ] 에이전트 대화 히스토리 관리
- [ ] 도구(tool) 확장
- [ ] 멀티 에이전트(agent swarm) 실험
