## Chapter 8: Prompt Crafting and Prompt Engineering for Copilot Chat — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | What does @workspace do in Copilot Chat? | Gives Copilot access to the indexed contents of the entire open project/repository for code search and Q&A, not just the active file. Exam tip: use for 'find where X is defined/used across the repo' scenarios. |
| 2 | What does @vscode do in Copilot Chat? | Scopes the chat to questions about the VS Code editor itself — settings, commands, keybindings, extensions. Exam tip: not for source code questions. |
| 3 | What does @github do in Copilot Chat? | Connects to GitHub-hosted data: issues, pull requests, discussions, repo metadata via the GitHub extension. Exam tip: required for any PR/issue summarization question. |
| 4 | Slash command to generate unit tests | /tests — generates test cases for selected code. Exam tip: distinct from /doc (docs) and /fix (bug fixes). |
| 5 | Slash command to explain selected code | /explain — produces a natural-language explanation of the selected code block. |
| 6 | Slash command to fix a problem in code | /fix — proposes a fix for errors/bugs in the selected code, often paired with an error the editor detects. |
| 7 | Slash command to generate documentation comments | /doc — inserts documentation comments (e.g., docstrings) for the selected function/class. |
| 8 | Slash command to simplify code | /simplify — rewrites selected code to be more concise/readable without changing behavior. |
| 9 | Zero-shot prompting definition | Asking the model to perform a task with a direct instruction and no examples provided. Exam tip: the default/simplest prompt style. |
| 10 | Few-shot prompting definition | Supplying one or more example input/output pairs in the prompt before the actual request, to steer format, style, or logic. Exam tip: use when output format consistency matters (e.g., commit messages, structured JSON). |
| 11 | Best practice when a Copilot Chat response is close but not correct? | Continue the SAME conversation with a specific follow-up correction (iterative refinement) rather than restarting a new chat — preserves context. Exam tip: iterative refinement is heavily tested. |
| 12 | Default context source when no @-participant is used | Copilot Chat uses the currently open/active editor tabs as implicit context. Full-repo context requires explicitly invoking @workspace. |
