## Chapter 2: Copilot in the IDE: Completions, Chat, Inline Chat, and Slash Commands — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Keyboard shortcut for inline chat in VS Code? | Ctrl+I (Cmd+I on macOS). Exam tip: distinguish from the Chat panel shortcut (Ctrl+Alt+I / Cmd+Shift+I). |
| 2 | What does /explain do? | Returns a natural-language explanation of selected code in chat. Does not modify code. |
| 3 | What does /fix do? | Proposes a code change to resolve an error, bug, or diagnostic in the selected code. |
| 4 | What does /tests do? | Generates unit test code for the selected function or file. |
| 5 | What does /doc do? | Generates documentation comments (e.g., docstrings) for the selected code. |
| 6 | Chat panel vs inline chat — core distinction? | Chat panel = persistent, broader multi-turn conversation view. Inline chat = scoped to cursor/selection for quick, in-place contextual edits. |
| 7 | What is 'ghost text' in Copilot? | The grayed-out inline code suggestion shown as you type; accept with Tab. This is the core completions feature, distinct from chat-based features. |
| 8 | What does having multiple related files open do for completions? | Copilot can use content from other open tabs as extra context, improving suggestion relevance to match existing patterns/signatures in the project. |
| 9 | What is Copilot Edits used for? | Multi-file, agent-style edits driven by a single natural-language request — e.g., renaming a function and updating all call sites across many files. |
| 10 | Which feature is best for a quick one-off explanation of a selected block without leaving the editor? | Inline chat with /explain — keeps focus in-place rather than switching to the side panel. |
| 11 | IDE feature parity: where do new Copilot features typically ship first? | VS Code typically receives new capabilities (like Copilot Edits) first; JetBrains and Visual Studio integrations may lag behind. |
| 12 | Is the Copilot Chat panel available in JetBrains IDEs? | Yes — the Chat panel is supported across VS Code, Visual Studio, and JetBrains IDEs, though feature parity for newer capabilities can vary. |
