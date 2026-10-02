## Chapter 2: Copilot in the IDE: Completions, Chat, Inline Chat, and Slash Commands — Practice Questions

**Q1.** A developer has a complex regular expression selected in the editor and wants a quick explanation without switching focus away from the code. Which feature is the BEST fit?

A) Use inline chat (Ctrl+I / Cmd+I) with /explain on the selection
B) Open the Copilot Chat panel and paste the regex
C) Hover over the code and wait for a tooltip
D) Create a new markdown file and describe the regex manually

<details>
<summary>Answer</summary>

**Correct: A**

Inline chat operates directly in the editor at the cursor/selection, keeping the developer in flow; /explain on a selection returns a contextual explanation right there.

**Why the others are wrong:**
- The Chat panel works but requires copy-pasting and switching visual context — not the most efficient choice when a selection already exists in-editor.
- Hover tooltips show type/definition info, not AI-generated explanations.
- Manual documentation doesn't use Copilot at all and wastes time.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A team wants Copilot to generate unit tests for a newly written function, directly targeting that function's edge cases. Which slash command should they use?

A) /doc
B) /fix
C) /tests
D) /explain

<details>
<summary>Answer</summary>

**Correct: C**

/tests instructs Copilot to generate unit test scaffolding and cases for the selected function or file.

**Why the others are wrong:**
- /doc generates documentation/comments, not test code.
- /fix targets diagnosed errors or bugs in code, not test generation.
- /explain returns a natural-language explanation of code, not tests.

</details>

---

**Q3.** In Visual Studio Code, what is the default keyboard shortcut to open inline chat at the current cursor position?

A) Ctrl+Shift+P / Cmd+Shift+P
B) Ctrl+I / Cmd+I
C) Ctrl+Alt+I / Cmd+Shift+I
D) Alt+/ 

<details>
<summary>Answer</summary>

**Correct: B**

Ctrl+I (Cmd+I on macOS) is the default shortcut for inline chat in VS Code.

**Why the others are wrong:**
- This opens the Command Palette, unrelated to Copilot.
- This shortcut opens the separate Copilot Chat panel, not inline chat.
- This is not a Copilot-related default shortcut.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A developer has three related files open in tabs: a controller, a service, and a test file. They start typing a new method in the controller. How does having the other files open affect Copilot's inline completions?

A) It has no effect — Copilot only reads the active file
B) Copilot may use content from the other open tabs as additional context to improve suggestion relevance
C) Copilot will automatically edit the service and test files too
D) Open tabs slow down completions but do not change their content

<details>
<summary>Answer</summary>

**Correct: B**

Copilot uses neighboring open tabs as contextual signals, which can improve the relevance of suggestions based on related code such as method signatures or existing patterns.

**Why the others are wrong:**
- Copilot is context-aware beyond just the active file for standard completions.
- Inline completions only affect the file being edited; multi-file changes require Copilot Edits, a separate feature.
- The effect is on relevance/quality of suggestions, not just performance.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which statement BEST describes the core difference between the Copilot Chat panel and inline chat?

A) The Chat panel only works in JetBrains IDEs, while inline chat only works in VS Code
B) The Chat panel is a persistent side conversation view for broader questions, while inline chat is scoped to a specific location in the code for quick, contextual edits
C) Inline chat requires a Copilot Business license, while the Chat panel is available on all plans
D) They are functionally identical, differing only in visual placement

<details>
<summary>Answer</summary>

**Correct: B**

The Chat panel supports ongoing, broader conversations (multiple turns, general questions, cross-file discussion), while inline chat is anchored to a cursor/selection for quick, in-place changes.

**Why the others are wrong:**
- Both features are available across supported IDEs (VS Code, Visual Studio, JetBrains), with some parity gaps but not an exclusive split.
- License tier does not gate inline chat vs. the Chat panel this way.
- They differ meaningfully in scope and workflow, not just visual placement.

</details>

---

**Q6.** A developer needs to rename a function and update every call site across 12 files in the project simultaneously using Copilot. Which feature should they use?

A) Inline chat run separately in each of the 12 files
B) Copilot Edits (multi-file agent mode)
C) The /fix slash command in the Chat panel
D) Ghost text completions triggered file by file

<details>
<summary>Answer</summary>

**Correct: B**

Copilot Edits is designed for coordinated multi-file changes, allowing a single natural-language request to propose and apply edits across multiple files at once.

**Why the others are wrong:**
- Running inline chat file-by-file is possible but inefficient and not the multi-file-optimized workflow the exam expects.
- /fix targets diagnosed problems in a single context, not coordinated cross-file renames.
- Ghost text completions are single-suggestion, single-location and not designed for coordinated refactors.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A developer selects a function with no comments and runs a slash command that returns a docstring-style comment block above the function. Which command did they use?

A) /explain
B) /tests
C) /fix
D) /doc

<details>
<summary>Answer</summary>

**Correct: D**

/doc generates documentation comments (e.g., docstrings) for the selected code.

**Why the others are wrong:**
- /explain produces a natural-language explanation in chat, not an inserted docstring.
- /tests generates test code, not documentation.
- /fix addresses errors/bugs, not documentation generation.

</details>

---

**Q8.** Which of the following is a known parity consideration when comparing Copilot in VS Code versus other supported IDEs (e.g., JetBrains, Visual Studio)?

A) Newer capabilities such as Copilot Edits and certain chat features may roll out to VS Code first, with JetBrains and Visual Studio receiving them later
B) Ghost text completions are exclusive to VS Code and unavailable elsewhere
C) Slash commands only function in the Chat panel and never in inline chat, regardless of IDE
D) The Copilot Chat panel is unavailable in JetBrains IDEs

<details>
<summary>Answer</summary>

**Correct: A**

GitHub has historically shipped newer Copilot capabilities to VS Code first, with other IDE integrations (JetBrains, Visual Studio) catching up afterward — a documented feature-parity gap.

**Why the others are wrong:**
- Ghost text completions are available across all supported IDEs, not exclusive to VS Code.
- Slash commands are usable in both the Chat panel and inline chat, depending on IDE support.
- The Chat panel is supported in JetBrains IDEs as well as VS Code and Visual Studio.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

