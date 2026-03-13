# AGENTS.md - AI Agent Operational Guidelines

This document outlines the protocols, standards, and workflows for AI agents (and human contributors) operating within the "大模型江湖" (Big Model Jianghu) repository.

## 1. Project Context & Mission

**Goal:** To objectively record, organize, and archive the history, development, and key events of Large Language Models (LLMs).
**Core Principle:** All content must be based on public internet search results. **NO secondary creation, NO malicious processing, NO subjective bias.**
**Language:** The primary language of the content is **Simplified Chinese (简体中文)**.
**License:** MIT License.

## 2. Repository Structure

Understanding the directory structure is crucial for placing new content correctly.

- **`timeline/`**: Chronological milestones.
    - *Naming:* `YYYY.md` (e.g., `2023.md`, `2024.md`) or `YYYY-MM.md` if granular.
    - *Content:* Release dates, major announcements.
- **`companies/`**: Profiles of organizations.
    - *Naming:* `CompanyName.md` (e.g., `OpenAI.md`, `Anthropic.md`).
    - *Content:* Founding date, key personnel, product portfolio.
- **`models/`**: Technical specifications of models.
    - *Naming:* `ModelName.md` (e.g., `GPT-4.md`, `Llama.md`).
    - *Content:* Parameter counts, context window, benchmarks, license type.
- **`events/`**: Industry-wide events, policy, and controversies.
    - *Naming:* `Topic.md` (e.g., `Regulation.md`, `Conferences.md`).

## 3. Contribution Workflow

When asked to add information:

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

## 4. Content Guidelines (Style & Tone)

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

## 5. Markdown Standards

### 5.1 Formatting
- **Headers:** Use ATX style (`#`, `##`). Hierarchy should be logical.
    - H1: File Title (Once per file)
    - H2: Major Sections
    - H3: Specific Items/Dates
- **Lists:** Use hyphens `-` for unordered lists.
- **Bold:** Use `**text**` for key entities (Company names, Model names) to improve scannability.
- **Code Blocks:** Use backticks for commands or JSON data.

### 5.2 Naming Conventions
- **Files:** PascalCase or camelCase for specific entities (`OpenAI.md`), kebab-case for general concepts (`knowledge-distillation.md`).
- **Directories:** lowercase, kebab-case (`companies`, `model-architectures`).
- **Images:** Place in an `assets/` folder (create if missing), use relative paths.

### 5.3 Tables
Use tables for comparing models or listing specs.

```markdown
| 模型名称 | 参数量 | 发布日期 | 许可证 |
| :--- | :--- | :--- | :--- |
| Llama 3 | 70B    | 2024-04  | Community License |
```

## 6. Build & Lint Commands

Since this is a documentation-only repository, "building" refers to rendering Markdown.

### 6.1 Linting (Recommended)
While not enforced by CI yet, agents should self-correct standard Markdown errors:
- Ensure blank lines around headers and lists.
- No trailing whitespace.
- Consistent indentation (2 or 4 spaces).

### 6.2 Testing Links
- Verify that all inserted URLs are valid and reachable.
- Ensure relative links between files (e.g., `[OpenAI](../companies/OpenAI.md)`) are correct.

## 7. Error Handling & Edge Cases

- **Conflicting Info:** If sources disagree on a date/number, note the discrepancy: "Source A states X, while Source B states Y."
- **Missing Info:** Use explicit placeholders like `(待补充)` or `TBD` rather than guessing.
- **Duplicate Entries:** Before adding an event, `grep` or search to ensure it hasn't been recorded in another file (e.g., checking if a model release is already in `timeline/2023.md` before creating `models/NewModel.md`).

## 8. Agent Behavior Rules

1.  **Read First:** Always read existing `README.md` in subdirectories to match the local style.
2.  **No Hallucinations:** If you don't know a parameter (e.g., context window size), do not invent one. Search or leave it blank.
3.  **Scoped Changes:** Only modify the files relevant to the user's request. Do not refactor the entire history unless asked.
4.  **Commit Messages:** (If asked to commit)
    - Format: `type(scope): description`
    - Types: `docs`, `feat`, `fix`, `style`.
    - Example: `docs(timeline): add GPT-4o release date`

## 9. Future Roadmap (For Awareness)

- **Static Site Generation:** The repo may eventually be built into a website (VitePress/Docusaurus). Keep frontmatter and structure clean to facilitate this migration.
- **Automation:** Future scripts may scrape data. Keep formatting consistent (e.g., always use `YYYY-MM-DD` for dates) to make parsing easier.

---
*This file is intended for AI agents to understand the operational context of the repository.*
