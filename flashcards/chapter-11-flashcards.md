## Chapter 11: Cross-Domain Review: Scenario-Based Judgment Drills — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Which Copilot plans support path-based content exclusion? | Business and Enterprise only. Individual and Pro/Pro+ do NOT support it. Exam tip: 'exclude paths from Copilot' = Business or Enterprise. |
| 2 | What triggers GitHub Copilot's public code matching filter? | Suggestions matching public code ≥150 characters. Toggled at org/enterprise level. Exam tip: this mitigates license/IP risk, not security bugs. |
| 3 | Which plan includes Knowledge Bases integrated with Copilot Chat on github.com? | Copilot Enterprise only. Business has Chat but not Knowledge Bases. Exam tip: 'searchable internal docs via chat' = Enterprise. |
| 4 | Where do admins configure Copilot content/duplication policies for Business/Enterprise? | Organization Settings → Copilot → Policies; Enterprise accounts can enforce these across all owned orgs. |
| 5 | Best practice for improving Copilot suggestion relevance? | Use descriptive comments and keep relevant files open for context. Exam tip: vague prompts = vague completions. |
| 6 | Who must review Copilot-generated code (including Autofix) before merge? | A human reviewer — AI suggestions are not guaranteed correct/secure. Exam tip: exam always favors human review over auto-merge. |
| 7 | Which plan supports centralized policy enforcement across multiple GitHub organizations? | Enterprise only. Business manages policies per single organization. Exam tip: 'multiple orgs, one policy' = Enterprise. |
| 8 | Do Copilot Business/Enterprise retain user code snippets to train GitHub's models? | No — prompts/suggestions are not used to train underlying models on Business/Enterprise. Individual users have a personal opt-in/out telemetry setting. |
| 9 | What is Copilot Autofix and where does it apply? | Suggests remediation for code scanning security alerts; tied to GitHub Advanced Security (Enterprise) and free for public repos. Exam tip: Autofix = security remediation, not general chat completions. |
| 10 | Exam tie-breaker rule for two similar 'correct-looking' scenario options? | Pick the option satisfying ALL stated constraints (cost, scale, security, plan). Partial matches are traps — re-read requirements before choosing. |
| 11 | What does the public code matching filter NOT protect against? | It does not detect security vulnerabilities or hallucinated APIs — only literal matches ≥150 chars to known public code. Don't confuse with Autofix or content exclusion. |
| 12 | Where/how is content exclusion configured? | Via repo/org settings using gitignore-style path patterns (e.g., .github/copilot config) to exclude files from both indexing and suggestions. Exam tip: excluded files are never used as context or suggested from. |
