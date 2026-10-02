## Chapter 3: Copilot in the CLI, GitHub.com, Pull Requests, and Extensions — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | gh copilot suggest — what does it do? | Generates a command from a natural-language description. Supports -t shell, -t git, -t gh to target the type of command. Exam tip: input = description, output = command. |
| 2 | gh copilot explain — what does it do? | Takes an existing command as input and returns a plain-language explanation of what it does. Exam tip: input = command, output = description (opposite direction of suggest). |
| 3 | How do you install GitHub Copilot in the CLI? | gh extension install github/gh-copilot — it's delivered as a gh CLI extension, not a separate install. |
| 4 | What are the three valid -t (target) values for gh copilot suggest/explain? | shell, git, gh — narrows the type of command Copilot generates or explains. |
| 5 | What does a GitHub Copilot knowledge base require? | GitHub Copilot Enterprise plan + explicitly indexed repositories. Without indexing, Chat cannot reference repo content even on Enterprise. |
| 6 | Which plan tier is required for Copilot knowledge bases? | Copilot Enterprise only — not available on Individual or Business. |
| 7 | Copilot pull request summaries — what do they generate? | An auto-drafted natural-language description of the code changes in a PR, triggered via the 'Ask Copilot' option when opening a pull request. |
| 8 | What does Copilot code review do? | Provides automated suggestions/comments on a pull request's diff when Copilot is requested as a reviewer — distinct from PR summaries, which describe the change rather than critique it. |
| 9 | What is a GitHub Copilot Extension? | A third-party integration invokable in Copilot Chat via @mention, built on GitHub Apps + Copilot API skillsets, bringing external tool data/actions into chat. |
| 10 | Scenario: Developer wants to bring a Jira-like tool into Copilot Chat via @mention. Which feature? | Copilot Extension — used for integrating third-party tools/services as chat agents, not knowledge bases (which only index GitHub repo content). |
| 11 | Scenario: Developer wants to know what a scary rm -rf command does before running it. Which command? | gh copilot explain — interprets existing commands; suggest would be wrong since there's no description to generate a command from. |
| 12 | Knowledge base vs Copilot Extension — key difference? | Knowledge base = indexed GitHub repo content used to answer Chat questions (Enterprise only). Extension = third-party service/tool integration invoked via @mention in Chat (separate mechanism, not repo-content based). |
