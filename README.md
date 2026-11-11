# Autonomous Python Developer (APD)

APD v0.1.0 is a local AI coding-agent prototype. The implementation package was prepared separately and includes a FastAPI dashboard, an OpenAI-compatible LLM adapter, workspace inspection, approval-gated file changes, SQLite task history, and Python compile/pytest checks.

## Runtime requirements
- Python 3.11+
- An OpenAI-compatible chat-completions endpoint (Ollama, OpenRouter, or OpenAI)

## Intended setup
Extract the APD source package, install the dependencies from `requirements.txt`, copy `.env.example` to `.env`, run `python -m apd doctor`, then start the local dashboard with `python -m apd serve`.

## Safety
Generated changes require human approval before writes. File operations are restricted to the configured workspace. Keep the server bound to localhost; do not expose it publicly.

## Repository status
This branch currently contains this project overview only. The complete source tree has **not** been pushed in this commit, and the README should not be treated as evidence that the repository is runnable yet.
