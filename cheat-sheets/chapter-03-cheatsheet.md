## Chapter 3 Cheat Sheet: CLI, GitHub.com, PRs, Extensions

### gh copilot CLI Commands
| Command | Input | Output | Target flag |
|---|---|---|---|
| `gh copilot suggest` | Natural-language description | A command to run | `-t shell\|git\|gh` |
| `gh copilot explain` | An existing command | Plain-language explanation | N/A (takes the command itself) |

Install via: `gh extension install github/gh-copilot`

**Memory trick:** *suggest* = "I have an idea, give me a command." *explain* = "I have a command, tell me what it does."

### Surface Selection Guide
| Task Described | Correct Surface |
|---|---|
| Generate a git/shell/gh command from description | `gh copilot suggest` |
| Understand an unfamiliar command | `gh copilot explain` |
| Ask questions about internal docs referencing private repo content | Copilot Chat + Knowledge Base (Enterprise) |
| Auto-draft a PR description | Copilot pull request summaries |
| Get automated feedback on a diff | Copilot code review |
| Integrate a third-party tool into chat via @mention | Copilot Extension |

### Knowledge Bases
- Require **GitHub Copilot Enterprise** — not available on Individual or Business.
- Repositories must be explicitly **indexed** by an org owner before Chat can reference their content.
- Used only within **Copilot Chat on GitHub.com** to ground answers in internal documentation.
- Common trap: assuming Business tier includes knowledge bases — it does not.

### PR Summaries vs Code Review
| Feature | Purpose | Trigger |
|---|---|---|
| PR Summaries | Describes *what changed* | "Ask Copilot" on PR creation |
| Code Review | Critiques/suggests improvements on the diff | Request Copilot as a reviewer |

Common trap: confusing "summarizing changes" (summaries) with "reviewing changes" (code review) — they are separate features with separate triggers.

### Copilot Extensions
- Third-party integrations invoked via `@extension-name` in Copilot Chat.
- Built on GitHub Apps + Copilot API skillsets.
- Can be private (org-internal) or public (GitHub Marketplace).
- Do **not** use repository indexing — that's exclusive to knowledge bases.

### Quick Decision Rule
- Repo content question → Knowledge Base (Enterprise + indexing)
- External tool/service question → Copilot Extension
- Command-line help → `gh copilot suggest`/`explain`
- PR text → Summaries (description) vs Code Review (critique)
