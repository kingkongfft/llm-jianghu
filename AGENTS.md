# AGENTS.md - AI Agent Operational Guidelines

This document outlines the protocols, standards, and workflows for AI agents (and human contributors) operating within the "大模型江湖" (Big Model Jianghu) repository.

## 1. Project Context & Mission

- **Goal:** To objectively record, organize, and archive the history, development, and key events of Large Language Models (LLMs).
- **Core Principle:** All content must be based on verified public information. **NO secondary creation, NO malicious processing, NO subjective bias.**
- **Language:** The primary language for documentation is **Simplified Chinese (简体中文)**.
- **License:** MIT License.

## 2. Repository Structure

Understanding the directory structure is crucial for placing new content correctly.

### Documentation (Core)
- **`timeline/`**: Chronological milestones.
    - *Naming:* `YYYY.md` (e.g., `2025.md`) or `YYYY-MM.md`.
    - *Content:* Release dates, major announcements.
- **`companies/`**: Profiles of organizations.
    - *Naming:* `CompanyName.md` (e.g., `OpenAI.md`, `DeepSeek.md`).
    - *Content:* Founding date, key personnel, product portfolio.
- **`classic-models/`**: Technical specifications of major models.
    - *Naming:* `ModelName.md` (e.g., `GPT-4o.md`, `DeepSeek-R1.md`).
    - *Content:* Parameter counts, context window, benchmarks, license type.
    - *Note:* Formerly `models/`, renamed to reflect the historical archiving nature.
- **`events/`**: Industry-wide events, policy, and controversies.
    - *Naming:* `Topic.md` (e.g., `OpenAI-Board-Crisis.md`).
- **`major_players.md`**: The central index file at the root, linking to companies and models.

### Tooling (Skills)
- **`.opencode/skills/`**: Python-based skills to automate research or repo maintenance.
    - Each skill resides in its own subdirectory (e.g., `ai-search/`).
    - Must contain a `SKILL.md` describing usage and a `requirements.txt`.

## 3. Contribution Workflow

### For Documentation
1.  **Search & Verify:**
    - Use the `ai-search` skill (`tavily_search.py`) to find authoritative sources (official blogs, papers).
    - **Crucial:** Verify dates, version numbers (e.g., v3 vs v3.5), and specific metrics (tokens, parameters).
2.  **Locate Target:**
    - Check `major_players.md` first to see where the entity belongs.
    - If a file exists, append new information chronologically.
3.  **Draft Content (Chinese):**
    - Write in objective Simplified Chinese.
    - Example: "OpenAI 于 2024 年 5 月发布了 GPT-4o..." (OpenAI released GPT-4o in May 2024...).
4.  **Link & Index:**
    - If creating a new file, ensure it is linked in `major_players.md` and the relevant `timeline/YYYY.md`.

### For Code (Python Skills)
1.  **Isolate:** Work within the specific skill directory.
2.  **Develop:** Write clean, typed Python code adhering to PEP 8.
3.  **Dependencies:** Update `requirements.txt` within the skill folder if adding libraries.

## 4. Documentation Standards

### 4.1 Neutrality & Tone
- **Do:** "DeepSeek-R1 在多个基准测试中得分超过 90分。" (DeepSeek-R1 scored over 90 on multiple benchmarks.)
- **Don't:** "DeepSeek-R1 是一个令人难以置信的、秒杀一切的神级模型。" (DeepSeek-R1 is an incredible, god-tier model that destroys everything.)

### 4.2 Markdown Conventions
- **Headers:** Use ATX style (`#`, `##`).
- **Links:** Use relative paths (e.g., `[GPT-4o](../classic-models/GPT-4o.md)`).
- **Tables:** Use for comparing model specs (e.g., Context Window, MMLU Score).
- **Bold:** Use `**text**` for key entities (Company names, Model versions).

## 5. Build, Lint & Test Commands

Since this is a hybrid repo (Docs + Python Tools), testing is scoped to the `skills` directory.

### 5.1 Python Environment
- **Setup:**
  ```bash
  # Inside a skill directory (e.g., .opencode/skills/ai-search/)
  pip install -r requirements.txt
  ```

### 5.2 Linting
- **Command:**
  ```bash
  flake8 .opencode/skills/
  # OR
  pylint .opencode/skills/**/*.py
  ```
- **Goal:** Ensure PEP 8 compliance.

### 5.3 Testing
- **Framework:** `unittest` is the standard.
- **Running a Single Test:**
  ```bash
  # Assuming a test file exists at .opencode/skills/ai-search/tests/test_search.py
  python -m unittest .opencode/skills/ai-search/tests/test_search.py
  ```
- **Note:** If no tests exist for a skill, create a `tests/` subdirectory and add basic unit tests before modifying the skill logic.

## 6. Code Style Guidelines (Python)

- **Formatting:** 4 spaces for indentation.
- **Typing:** Mandatory type hints for all function signatures.
  ```python
  def search(query: str, max_results: int = 5) -> List[Dict[str, Any]]:
      ...
  ```
- **Naming:**
  - Variables/Functions: `snake_case`
  - Classes: `PascalCase`
  - Constants: `UPPER_CASE`
- **Imports:**
  - Standard library first (e.g., `import json`, `import os`)
  - Third-party second (e.g., `import requests`)
  - Local imports last
- **Error Handling:** Catch specific exceptions (`requests.RequestException`) and provide informative error messages.

## 7. Agent Behavior Rules

1.  **Read First:** Always read `major_players.md` and `README.md` to understand the current state.
2.  **No Hallucinations:** If a parameter (like parameter count) is unknown, state "Unknown" or "Undisclosed" (e.g., "参数量: 未公开"). Do not guess.
3.  **Cross-Link:** When adding a model, link it to its company in `companies/` and the year in `timeline/`.
4.  **Commit Messages:**
    - Format: `type(scope): description`
    - Types: `docs` (documentation), `feat` (new skill/feature), `fix` (bug fix), `refactor` (structure change).
    - Example: `docs(classic-models): add DeepSeek-R1 technical specs`

## 8. Security Red Lines (CRITICAL)

1.  **NO SECRETS:** **Do not commit or push any password, API key, token, or secret credential to the repository.**
2.  **No `.env` Files:** Ensure that configuration files containing secrets are ignored.
3.  **Public Visibility:** This is a public repository. Assume all committed data is compromised immediately.

---
*This file is intended for AI agents to understand the operational context of the repository.*
