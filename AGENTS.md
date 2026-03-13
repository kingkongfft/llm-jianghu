# AGENTS.md - AI Agent Operational Guidelines

This document outlines the protocols, standards, and workflows for AI agents (and human contributors) operating within the "大模型江湖" (Big Model Jianghu) repository.

## 1. Project Context & Mission

**Goal:** To objectively record, organize, and archive the history, development, and key events of Large Language Models (LLMs).
**Core Principle:** All content must be based on public internet search results. **NO secondary creation, NO malicious processing, NO subjective bias.**
**Language:** The primary language of the content is **Simplified Chinese (简体中文)**.
**License:** MIT License.

## 2. Repository Structure

Understanding the directory structure is crucial for placing new content correctly.

### Documentation (Core)
- **`timeline/`**: Chronological milestones.
    - *Naming:* `YYYY.md` (e.g., `2023.md`, `2024.md`) or `YYYY-MM.md`.
    - *Content:* Release dates, major announcements.
- **`companies/`**: Profiles of organizations.
    - *Naming:* `CompanyName.md` (e.g., `OpenAI.md`, `Anthropic.md`).
    - *Content:* Founding date, key personnel, product portfolio.
- **`models/`**: Technical specifications of models.
    - *Naming:* `ModelName.md` (e.g., `GPT-4.md`, `Llama.md`).
    - *Content:* Parameter counts, context window, benchmarks, license type.
- **`events/`**: Industry-wide events, policy, and controversies.
    - *Naming:* `Topic.md` (e.g., `Regulation.md`, `Conferences.md`).

### Tooling (Skills)
- **`.opencode/skills/`**: Python-based skills to automate research or repo maintenance.
    - Each skill resides in its own subdirectory (e.g., `ai-search/`).
    - Must contain a `SKILL.md` describing usage.

## 3. Contribution Workflow

### For Documentation
1.  **Search & Verify:**
    - Use search tools to find authoritative sources (official blogs, reputable news, papers).
    - Cross-reference dates and specific numbers (parameters, scores).
2.  **Locate Target:**
    - Identify the most appropriate directory.
    - If a file exists, append to it. If not, create a new file following the naming convention.
3.  **Draft Content:**
    - Write in neutral, objective tone.
    - Cite sources where possible (as hyperlinks).
4.  **Review:**
    - Check against "Content Guidelines" below.

### For Code (Python Skills)
1.  **Isolate:** Work within the specific skill directory in `.opencode/skills/`.
2.  **Develop:** Write clean, typed Python code.
3.  **Test:** Create and run unit tests to verify functionality.
4.  **Document:** Update `SKILL.md` if usage changes.

## 4. Documentation Guidelines (Style & Tone)

### 4.1 Neutrality
- **Do:** "OpenAI released GPT-4 on March 14, 2023."
- **Don't:** "OpenAI released the mind-blowing GPT-4 which destroyed all competition."
- Avoid adjectives like "revolutionary", "insane", "game-changing" unless quoting a source directly.

### 4.2 Accuracy
- Distinguish between **rumors** and **official announcements**.
- If a date is uncertain, mark it as "Est." or "Rumored".
- Verify model parameters (e.g., "175B" vs "Dense/MoE").

### 4.3 Sourcing
- Prefer primary sources: arXiv papers, official company blogs, GitHub repos.
- Secondary sources: TechCrunch, The Verge, reputable tech media.
- Format: `[Source Name](URL)` or purely as a reference link.

### 4.4 Markdown Standards
- **Headers:** Use ATX style (`#`, `##`). Hierarchy should be logical.
- **Lists:** Use hyphens `-` for unordered lists.
- **Bold:** Use `**text**` for key entities (Company names, Model names).
- **Code Blocks:** Use backticks for commands or JSON data.
- **Tables:** Use tables for comparing models or listing specs.

## 5. Coding Guidelines (Python Skills)

When modifying or adding Python scripts in `.opencode/skills/`:

### 5.1 Style & Formatting
- **PEP 8:** Follow standard Python style guidelines.
- **Imports:** Group imports: standard library, third-party, local.
- **Typing:** Use type hints (`typing` module) for all function arguments and return values.
  ```python
  def fetch_data(url: str, timeout: int = 10) -> dict[str, Any]:
      ...
  ```
- **Naming:**
  - Variables/Functions: `snake_case`
  - Classes: `PascalCase`
  - Constants: `UPPER_CASE`

### 5.2 Error Handling
- Use specific exception types (e.g., `ValueError`, `requests.HTTPError`) rather than bare `except:`.
- Provide meaningful error messages that help debug the issue.
- Gracefully handle API failures (e.g., timeouts, rate limits).

### 5.3 Testing
- **Framework:** Use `unittest` for testing skills.
- **Location:** Place tests in the same directory or a `tests/` subdirectory within the skill folder.
- **Mocking:** Mock external API calls to avoid hitting live endpoints during tests.
- **Command:** Run a single test file using:
  ```bash
  python .opencode/skills/<skill-name>/scripts/test_script.py
  ```

### 5.4 Dependencies
- **Isolation:** Each skill should declare its dependencies.
- **File:** Maintain a `requirements.txt` in the skill's root directory if external packages are used.
- **Version:** Pin major versions where possible (e.g., `requests>=2.31.0`).

## 6. Build & Lint Commands

Since this is a hybrid repo (Docs + Python Tools):

### 6.1 Documentation Linting
- Ensure blank lines around headers and lists.
- No trailing whitespace.
- Consistent indentation (2 or 4 spaces).
- Verify all links are valid.

### 6.2 Python Linting & Testing
- **Lint:** (If available) `flake8 .opencode/skills/` or `pylint`.
- **Test:** Run specific test scripts as needed.
  ```bash
  # Example: Run tests for ai-search
  python -m unittest .opencode/skills/ai-search/scripts/test_tavily_search.py
  ```

## 7. Error Handling & Edge Cases

- **Conflicting Info (Docs):** If sources disagree, note the discrepancy: "Source A states X, while Source B states Y."
- **Missing Info (Docs):** Use explicit placeholders like `(待补充)` or `TBD`.
- **Duplicate Entries:** `grep` before adding to avoid redundancy.

## 8. Agent Behavior Rules

1.  **Read First:** Always read existing `README.md` or `SKILL.md` to understand context.
2.  **No Hallucinations:** If you don't know a parameter, do not invent one. Search or leave it blank.
3.  **Scoped Changes:** Only modify the files relevant to the user's request.
4.  **Commit Messages:**
    - Format: `type(scope): description`
    - Types: `docs` (documentation), `feat` (new skill/feature), `fix` (bug fix), `style` (formatting).
    - Example: `docs(timeline): add GPT-4o release date` or `fix(ai-search): handle API timeout`

---
*This file is intended for AI agents to understand the operational context of the repository.*
