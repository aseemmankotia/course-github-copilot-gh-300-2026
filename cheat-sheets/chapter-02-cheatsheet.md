## Chapter 2 Cheat Sheet: Copilot in the IDE

### Slash Commands
| Command | Action | Output Location |
|---|---|---|
| /explain | Explains selected code in plain language | Chat response (no code change) |
| /fix | Proposes a fix for an error/bug in selection | Suggested diff/edit |
| /tests | Generates unit tests for selected code | New test code |
| /doc | Generates documentation/docstring comments | Inserted comment block |

**Exam trap:** /explain and /doc are often confused — /explain talks *about* the code in chat; /doc *writes* a comment into the code.

### Chat Panel vs Inline Chat
| Feature | Chat Panel | Inline Chat |
|---|---|---|
| Scope | Whole conversation, cross-file, multi-turn | Anchored to cursor/selection |
| Shortcut (VS Code) | Ctrl+Alt+I / Cmd+Shift+I | Ctrl+I / Cmd+I |
| Best for | Broad questions, architecture discussion, longer back-and-forth | Quick in-place explain/fix/edit without leaving code |
| Output | Appears in side panel | Appears as inline diff/suggestion at cursor |

### Core Completion Feature
- **Ghost text** = inline gray-text suggestion as you type. Accept with Tab.
- Distinct from chat features — no prompt needed, purely context-driven.

### Context Awareness
- Copilot considers the **active file** plus signals from **other open tabs** to improve relevance (e.g., matching naming conventions, related function signatures).
- Closing irrelevant tabs and keeping related files open can improve suggestion quality — a scenario the exam may test indirectly.

### Copilot Edits (Multi-file)
- Use for coordinated changes across **multiple files** from a single natural-language request (e.g., rename + update all call sites).
- Distinguish from inline chat (single location) and Chat panel (conversation only, no direct multi-file edit application in older versions).

### IDE Parity Notes
- Supported IDEs: VS Code, Visual Studio, JetBrains family (and others via extensions).
- **New features typically land in VS Code first**, then roll out to JetBrains/Visual Studio later — a common parity-gap exam point.
- Core features (ghost text, Chat panel, inline chat, slash commands) are broadly available across major supported IDEs, but exact command palette integration and UI can differ.

### Quick Decision Rule
- Need explanation only → **/explain** (inline chat or panel)
- Need broken code fixed → **/fix**
- Need tests written → **/tests**
- Need comments/docstring → **/doc**
- Need change across many files → **Copilot Edits**, not inline chat
