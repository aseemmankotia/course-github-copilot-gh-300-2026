## Copilot Chat Prompt Crafting — Cheat Sheet

### @-Participants
| Participant | Scope | Use When |
|---|---|---|
| @workspace | Indexed local project/repo source | Finding refs/definitions across many files |
| @vscode | Editor commands, settings, keybindings | Questions about VS Code itself |
| @github | GitHub issues, PRs, discussions, repo metadata | Summarizing/querying GitHub-hosted data |
| (none) | Currently open/active editor tabs only | Quick question about visible code |

**Exam note:** @workspace ≠ @github. @workspace = local code index. @github = remote GitHub data via API/extension.

### Slash Commands
| Command | Purpose |
|---|---|
| /explain | Explain selected code in plain language |
| /fix | Propose a fix for detected problems |
| /tests | Generate unit tests for selected code |
| /doc | Generate documentation comments |
| /simplify | Rewrite code more concisely |
| /help | Show Copilot Chat help/usage |
| /clear | Clear current chat session |

**Common mistake:** Confusing /doc (adds comments) with /explain (returns a chat explanation, doesn't modify code).

### Zero-shot vs Few-shot
| Pattern | Structure | Best For |
|---|---|---|
| Zero-shot | Instruction only, no examples | Simple, well-known tasks (e.g., "write a bubble sort") |
| Few-shot | 1+ input/output examples, then the request | Enforcing a specific format/style (commit messages, structured output, custom naming conventions) |

**Exam note:** If a question emphasizes matching an existing format/convention, the correct pattern is few-shot, not zero-shot.

### Context & Specificity Rules
- Vague prompt ("fix this") → weak/generic response. Specific prompt ("fix the null pointer exception on line 42 when input is empty") → targeted response.
- Open files in tabs are automatically part of context; closing irrelevant tabs improves prompt accuracy.
- Use @workspace when the answer might live outside the currently open file(s).
- Iterative refinement = continue the SAME thread with a corrective, specific follow-up rather than restarting.

### Common Exam Traps
1. Assuming @workspace searches GitHub issues/PRs (it does not — that's @github).
2. Assuming Copilot Chat has zero context without any @-participant (it still uses open tabs).
3. Choosing zero-shot when the scenario clearly asks to match example-driven formatting (few-shot is correct).
