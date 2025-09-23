# Copilot Instructions for MedicalChatbotLang

## Project Overview
- **MedicalChatbotLang** is a Python project for building a medical chatbot using LLMs, vector search, and Flask APIs.
- The codebase is organized for modularity: core logic in `src/`, research notebooks in `research/`, and entry points/scripts at the root.

## Key Components
- `src/` — Place for all Python modules. Typical files: `helper.py`, `prompt.py`. These may be empty templates initially.
- `app.py` — Intended as the main Flask app entry point. (May be empty at project start.)
- `requirements.txt` — All dependencies, including `langchain`, `flask`, `sentence-transformers`, `pypdf`, and integrations for Pinecone and OpenAI.
- `.env` — Must contain `PINECONE_API_KEY` and `OPENAI_API_KEY` for external service access.
- `research/` — For Jupyter notebooks and experiments.

## Setup & Developer Workflow
1. **Environment**: Use Python 3.10 (see README for conda instructions).
2. **Install dependencies**: `pip install -r requirements.txt`
3. **Configure secrets**: Add `.env` with Pinecone/OpenAI keys.
4. **Run the app**: `python app.py` (Flask server expected, but app.py may need implementation).
5. **(Optional) Research**: Use `research/trials.ipynb` for prototyping.

## Patterns & Conventions
- All new logic should go in `src/` modules, not in the root.
- Use environment variables for all credentials and API keys.
- Follow modular design: keep helpers, prompts, and business logic separated.
- Use `requirements.txt` for all Python dependencies; update as needed.
- If adding new scripts, document their usage in the README.

## Integration Points
- **Pinecone**: For vector storage/indexing (see `.env` and requirements).
- **OpenAI**: For LLM completions (see `.env` and requirements).
- **Flask**: For serving the chatbot API (expected in `app.py`).

## Example: Adding a New Helper
- Add logic to `src/helper.py`.
- Import in `app.py` as needed.
- Document any new scripts or endpoints in the README.

## Troubleshooting
- If `app.py` is empty, you may need to implement the Flask app structure.
- If you see missing key errors, check `.env` for required API keys.

---
For any unclear conventions or missing documentation, check the README or ask for clarification.
