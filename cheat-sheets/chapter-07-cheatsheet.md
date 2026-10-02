## Chapter 7 Cheat Sheet: Developer Use Cases for AI

### Slash Commands (Copilot Chat)
| Command | Purpose | Exam Note |
|---|---|---|
| `/explain` | Describes what code does, no changes | Use FIRST on unfamiliar/legacy code |
| `/fix` | Proposes a bug fix | No guarantee of correctness — review required |
| `/tests` | Generates unit tests | Not the same as `/doc` |
| `/doc` | Generates doc comments/docstrings | Not full README/external docs |
| `/simplify` | Simplifies existing code | Different from refactor (broader restructuring) |
| `/optimize` | Suggests performance improvements | Test before trusting perf claims |
| *(none)* | Language translation | No dedicated command — ask Chat directly, name target language |

### Choosing the Right Use Case
| Situation | Best Approach |
|---|---|
| Unfamiliar/legacy code | `/explain` before touching anything |
| Need same behavior, better structure | Refactor |
| Moving logic to a new language | Copilot Chat conversational translation |
| New project/repo | Scaffolding/boilerplate generation |
| Writing tests | `/tests` |
| Writing commit message | VS Code Source Control sparkle icon |
| Writing PR description | Copilot for Pull Requests (PR summary) |

### When AI Assistance Is NOT Appropriate
- Security-critical/cryptographic implementations without expert + library review
- Compliance-driven business logic requiring guaranteed correctness
- Debugging issues dependent on runtime state, logs, or timing (Copilot has no execution visibility)
- Proprietary algorithms where exact business rules must be authoritative, not inferred

### Debugging Limits
Copilot reasons only from the code/text given to it. It cannot:
- Access logs, metrics, or live runtime state
- Reproduce timing-dependent/concurrency bugs
- Guarantee a fix resolves production behavior — always verify with tests

### Documentation & Commit Messages
- **Commit message**: VS Code Source Control panel → sparkle icon → generates message from staged diff
- **PR description**: Copilot for Pull Requests → summarizes diff into title + description
- **Code docs**: `/doc` for docstrings/comments on selected code

### Common Exam Traps
- Assuming a `/translate` command exists (it doesn't — use Chat conversationally)
- Choosing 'refactor' when 'explain' is the correct first step for unfamiliar code
- Trusting `/fix` as a security or correctness guarantee
- Assuming AI should be disabled entirely for a security-sensitive project instead of scoping its use appropriately
