## Chapter 6: Privacy Fundamentals and Context Exclusions — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Which GitHub Copilot plans support content exclusions? | Business and Enterprise only. Free and Pro (Individual) do NOT support content exclusions. Exam tip: solo-developer scenarios needing exclusions require an upgrade. |
| 2 | What are the two configuration levels for content exclusion? | Organization-level (set by org owners, org-wide) and Repository-level (set by repo admins, only if org policy permits it). |
| 3 | If an org disables repo-level exclusion configuration, what happens to existing repo-level rules? | They are ignored/not enforced. Only org-level rules apply. |
| 4 | What is the duplication-detection filter setting called? | 'Suggestions matching public code' — set to Block or Allow at the org level (Business/Enterprise). |
| 5 | Does content exclusion hide or delete the file from the repository? | No. It only prevents the file's content from being used as Copilot context/suggestions; the file remains fully accessible. |
| 6 | GitHub Copilot Business/Enterprise data training commitment? | Prompts and suggestions are NOT used to train GitHub's models — this is contractual, not a toggle. |
| 7 | How to verify content exclusion is active in VS Code? | Check the Copilot status bar icon — it changes and shows a message when the current file is excluded from context. |
| 8 | What syntax is used for content exclusion paths? | Gitignore-style glob patterns defined per repo name with a 'paths' array, e.g. /secrets/**. |
| 9 | Does content exclusion affect Copilot Chat too? | Yes — excluded content is blocked from use as context in Copilot Chat, not just inline code suggestions. |
| 10 | Repo-level vs org-level exclusion precedence rule | Org-level rules always apply; repo-level rules only take effect if the org allows repository-level exclusion configuration. |
| 11 | Copilot Individual telemetry setting | Individual/Pro users can opt in/out of 'Allow GitHub to use my code snippets for product improvements.' No equivalent toggle exists for Business/Enterprise since training use is already excluded by default. |
| 12 | Exam weight of Privacy Fundamentals and Context Exclusions domain? | 15% of the GH-300 exam. |
