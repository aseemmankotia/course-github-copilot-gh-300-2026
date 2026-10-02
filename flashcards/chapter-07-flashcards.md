## Chapter 7: Developer Use Cases for AI Pair Programming — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Which Copilot slash command generates unit tests for selected code? | /tests — exam tip: distinguish from /doc (docs) and /explain (description only, no test output) |
| 2 | Which Copilot slash command explains what a code block does? | /explain — use BEFORE refactoring/translating unfamiliar or legacy code. Exam tip: explain = understand, no code changes made |
| 3 | Which Copilot slash command proposes a fix for a bug/error? | /fix — exam tip: does not guarantee correctness, still requires developer review, especially for concurrency/runtime bugs |
| 4 | Which Copilot slash command generates documentation comments? | /doc — exam tip: generates docstrings/inline comments, not full external docs like README files |
| 5 | Is there a dedicated Copilot slash command for translating code between languages? | No — ask Copilot Chat conversationally, naming the target language. Exam trap: students assume a /translate command exists |
| 6 | Where in VS Code do you generate an AI commit message from staged changes? | Source Control panel — click the sparkle/Copilot icon next to the commit message box |
| 7 | What Copilot feature auto-generates a PR title and description? | Copilot for Pull Requests (PR summary) — reads the diff and drafts description. Exam tip: separate from VS Code commit message generation |
| 8 | Refactor vs Explain — key exam distinction? | Explain = describes existing code, no changes made. Refactor = restructures code while preserving behavior. Exam tip: use explain FIRST on unfamiliar/legacy code |
| 9 | Scenario: security-critical cryptographic function — is Copilot appropriate as sole author? | No — use vetted libraries plus expert/security review. AI-authored crypto without review is a classic 'not appropriate' exam trap |
| 10 | Why can't Copilot reliably fix an intermittent concurrency bug? | It has no access to runtime state, logs, or execution history — reasoning is limited to the static code/text pasted into it |
| 11 | Best Copilot use case for a brand-new Express.js API project? | Scaffolding/boilerplate generation — Copilot Chat or inline suggestions quickly generate initial project structure and routes |
| 12 | When should you NOT rely on a Copilot suggestion without deep human review? | Security-critical code, compliance-driven logic, and proprietary business-critical algorithms — always require expert review regardless of AI confidence |
