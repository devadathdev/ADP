# Autonomous Python Developer (APD)

APD v0.1.0 is a local AI coding agent that plans changes, presents complete proposed file contents, requires explicit human approval before writing, and runs Python compilation and pytest checks.

## Source package

The complete source package is available at [APD v0.1.0 ZIP](./APD-v0.1.0.zip). Extract it, then follow the included README for setup and configuration.

## Stack
- FastAPI local dashboard
- OpenAI-compatible LLM endpoint (Ollama, OpenRouter, or OpenAI)
- SQLite task history
- Workspace-scoped file operations and path traversal protection
- Approval-gated writes
- compileall and pytest verification

## Quick start (Windows PowerShell)
```powershell
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
Copy-Item .env.example .env
python -m apd doctor
python -m apd serve
```

Open http://127.0.0.1:8765. Review generated changes before approving them. Keep the local server bound to localhost; do not expose it publicly.

## Status
Initial implementation committed for review. Syntax compilation was checked when packaged; provider integration and full runtime tests still need to be run in the target environment.
