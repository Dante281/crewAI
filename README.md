# CrewAI – PrimeCrew

First fully working **CrewAI** project using **Groq** as the LLM provider and **LiteLLM** as the integration layer. This repository demonstrates an end‑to‑end flow with YAML‑defined agents, CLI execution, and dependency management via **uv**.

## Features

* CrewAI 1.7.x
* LLM Provider: **Groq**
* Dependency management: **uv**
* YAML‑based configuration (`agents.yaml`, `tasks.yaml`)
* Sensitive variables isolated in `.env`

## Project Structure

```
primecrew/
├─ src/primecrew/
│  ├─ config/
│  │  ├─ agents.yaml
│  │  └─ tasks.yaml
│  ├─ crew.py
│  └─ main.py
├─ knowledge/
├─ .gitignore
├─ pyproject.toml
├─ uv.lock
└─ README.md
```

## Requirements

* Python 3.12
* uv
* Groq account and API key

## Installation

```bash
# create and sync the environment
uv sync

# activate the virtual environment
source .venv/bin/activate
```

## Configuration

Create a `.env` file at the project root (not versioned):

```env
GROQ_API_KEY=your_api_key_here
MODEL=groq/llama-3.3-70b-versatile
```

## Running the Crew

```bash
crewai run
```

## Notes

* This project is intended as a base for experimenting with multiple crews.
* Always add dependencies using `uv add <package>`.
* The `.env` file is excluded from version control for security reasons.

## Status

✅ First successful end‑to‑end CrewAI run completed.

---

Author: Dante281
