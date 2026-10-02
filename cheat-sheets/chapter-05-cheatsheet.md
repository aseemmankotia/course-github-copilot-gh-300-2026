## Chapter 5 Cheat Sheet: Copilot Internals & Data Handling (15% of exam)

### Request/Response Flow
1. Editor captures context (cursor position, open tabs, file path, language)
2. Client builds a **prompt** from that context
3. Prompt sent to Copilot backend (proxy) → routed to the selected LLM
4. Backend runs the response through **content filters** (toxicity, security patterns) and the **matching public code filter**
5. Filtered suggestion returned to the IDE

### What's Sent vs Excluded
| Included in context | Excluded from context |
|---|---|
| Current file content near cursor | Files matched by org Copilot content exclusion / `.copilotignore` |
| Snippets from neighboring **open** tabs | Files not open in the editor |
| File path & language metadata | `.gitignore` entries (NOT respected by Copilot — trap!) |
| Chat: explicit user query + selected knowledge base index (Enterprise) | Repo files outside the knowledge base index scope |

### Data Retention by Plan
| Plan | Used for model training? | Retention |
|---|---|---|
| Individual | Optional — user can opt IN via settings | Per opted setting |
| Business | No | Transient only (e.g., abuse/security review) |
| Enterprise | No | Transient only (e.g., abuse/security review) |

### Key Filters
| Filter | Purpose | Configurable? |
|---|---|---|
| Matching public code (duplication detection) | Flags suggestions closely matching public source; Block or Allow (with citation) | Yes — org/enterprise policy |
| Content filter (toxicity/security) | Blocks offensive language and known-insecure code patterns (hardcoded secrets, injection templates) | Not user-configurable |
| Content exclusion | Prevents specified paths/repos from being sent as context at all | Yes — org policy / `.copilotignore` |

### Underlying Models
- Originally built on **OpenAI Codex** (GPT-3 code-tuned)
- Modern Copilot Chat supports a **model picker**: OpenAI GPT models, Anthropic Claude, Google Gemini (availability varies by plan)

### Enterprise Knowledge Bases
- Semantic index over selected org repos/docs
- Lets Copilot Chat answer questions using private org context beyond open files
- Enterprise-only capability

### Exam Traps
- **`.gitignore` ≠ Copilot exclusion.** Only org content-exclusion rules or `.copilotignore` remove context.
- Business ≠ Individual on training: Business/Enterprise never train on customer code; Individual has an opt-in toggle.
- Matching public code filter is about **output** (suggestion vs public source); content exclusion is about **input** (what context is sent).
- Knowledge bases are Enterprise-only — don't confuse with basic open-tab context used in Business/Individual.
