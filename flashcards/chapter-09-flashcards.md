## Chapter 9: Testing with GitHub Copilot — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | What does the /tests slash command do in GitHub Copilot Chat? | Generates unit tests for the currently selected code or open file context. Exam tip: scope is limited to selection/context, not the whole repository. |
| 2 | A Copilot-generated test passes but the function's real behavior is wrong. What's the likely cause? | Missing or weak assertions — a false positive. Always inspect generated tests to confirm they assert meaningful outcomes before merging. |
| 3 | How do you get Copilot to generate boundary/edge-case tests instead of just happy-path tests? | Give explicit prompt instructions, e.g. 'generate tests for empty input, max length, and tier boundary values.' Generic /tests calls often skip edge cases by default. |
| 4 | What determines the scope of code analyzed when you run /tests? | The currently selected code or the open file's context — not the entire repository and not a config file. |
| 5 | Best way to get realistic fixture/mock data from Copilot for a test suite? | Provide the relevant type/schema definitions as context and ask Copilot Chat to generate fixture data matching that schema. |
| 6 | Copilot /tests vs Copilot Autofix — which one generates unit tests? | /tests generates unit tests for selected code. Autofix generates remediation suggestions for flagged security/code-scanning issues — it does not generate tests. |
| 7 | What must happen before merging any Copilot-generated test suite? | Human code review: confirm assertions exist, are meaningful, and edge cases are covered. Never merge AI-generated tests unreviewed. |
| 8 | Example prompt to force boundary-value test generation with Copilot Chat? | "Generate unit tests for [function] covering boundary values at each tier transition, empty input, and invalid input." Being specific closes common coverage gaps. |
| 9 | Name two common coverage gaps left by Copilot's default /tests output. | 1) Edge cases / boundary conditions, 2) invalid or malformed input handling. Default generation tends to favor the happy path. |
| 10 | Copilot Chat vs Copilot Workspace — which is used for iterative unit test generation on a single function? | Copilot Chat (via /tests) is used for targeted unit test generation. Copilot Workspace is for planning/implementing broader multi-file changes. |
| 11 | How should you iteratively improve code coverage using Copilot? | Run /tests, review resulting coverage, then re-prompt Copilot with specific gaps identified (e.g., 'add tests for null input') rather than accepting the first output as final. |
| 12 | Can you tell Copilot which test framework to use when generating tests? | Yes — specify it in the prompt (e.g., 'generate these tests using pytest' or 'using Jest'). Copilot otherwise infers the framework from existing project context. |
