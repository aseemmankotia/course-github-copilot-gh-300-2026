## Chapter 5: How GitHub Copilot Works and Handles Data — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Does GitHub Copilot Business use customer code to train the underlying model? | No — Business and Enterprise exclude customer prompts/suggestions from model training by default. Exam tip: this is the key distinction vs. Individual's opt-in setting. |
| 2 | What does the matching public code filter do? | Detects suggestions that closely match public source code and either blocks or shows them with a citation, per org policy (Block vs Allow). |
| 3 | Does .gitignore exclude files from Copilot's context? | No. .gitignore only affects git tracking. Only Copilot content exclusion (org policy / .copilotignore) removes files from context — a classic exam trap. |
| 4 | Which model providers can power Copilot Chat via the model picker? | OpenAI (GPT models), Anthropic (Claude), and Google (Gemini) can be selected depending on plan and settings. Exam tip: Copilot is not locked to a single vendor. |
| 5 | What context sources feed an inline completion prompt? | Current file content near the cursor, snippets from neighboring open tabs, file path, and language ID. Excludes closed/unopened and content-excluded files. |
| 6 | What is a Copilot Enterprise 'Knowledge Base'? | A semantic index of selected org repositories/docs enabling Copilot Chat to retrieve private organizational context beyond open editor files. Enterprise-only feature. |
| 7 | What does Copilot's content filtering system screen for? | Offensive/toxic language and known insecure code patterns (e.g., hardcoded secrets, injection-prone templates) — separate from the public-code-matching filter. |
| 8 | Which plan allows opting IN to share code for product improvement/training? | Copilot Individual only, via personal settings. Business/Enterprise never use customer code for training regardless of setting. |
| 9 | Where do you configure the org-wide 'suggestions matching public code' policy? | Organization/Enterprise settings > Copilot policies > Suggestions matching public code (Block or Allow). Admin-level, not per-repo. |
| 10 | What happens to Business/Enterprise prompts and suggestions data after a request completes? | Not retained for training; used only transiently for operational purposes such as abuse/security detection, per GitHub's data handling terms. |
| 11 | What actually excludes a file path from being used as Copilot context in an org? | A path match in the org's Copilot content exclusion policy (repo or org level) — not .gitignore. Frequently confused on the exam. |
| 12 | What was Copilot's original foundational model family? | OpenAI Codex, a GPT-3 code-tuned descendant. Legacy fact — current Copilot supports multiple model providers via the model picker. |
