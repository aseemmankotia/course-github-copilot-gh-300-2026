## Chapter 7: Developer Use Cases for AI Pair Programming — Practice Questions

**Q1.** A developer is assigned to modify a 2,000-line legacy Perl script with no documentation and no original author available. Before making any changes, what is the BEST first use of GitHub Copilot?

A) Ask Copilot to refactor the entire script in one pass to modernize it
B) Ask Copilot to translate the script to Python immediately
C) Skip Copilot and rewrite the script from scratch
D) Use Copilot Chat's /explain on specific functions to understand the logic before making any changes

<details>
<summary>Answer</summary>

**Correct: D**

/explain surfaces intent and logic without altering behavior — the critical first step before modifying unfamiliar legacy code.

**Why the others are wrong:**
- Refactoring before understanding risks breaking untested legacy behavior and hiding regressions.
- Translating before understanding carries the same risk — semantics can shift before functionality is verified.
- Discards working logic and ignores AI assistance entirely; not the best use of Copilot.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A team is implementing a custom encryption key-derivation function for a payments system. Which statement BEST describes appropriate Copilot use here?

A) Copilot suggestions should not be trusted as the sole source for security-critical cryptographic logic without expert review and vetted libraries
B) Copilot should generate the full implementation since it has seen many crypto examples
C) Copilot Chat's /fix command guarantees the implementation is secure
D) AI assistance should be disabled entirely for the whole payments project

<details>
<summary>Answer</summary>

**Correct: A**

Security-critical crypto is a classic 'AI not appropriate as sole author' case — use vetted libraries plus expert/security review.

**Why the others are wrong:**
- Relying solely on suggestions risks subtle vulnerabilities; Copilot has no guarantee of cryptographic correctness.
- /fix addresses code errors, not security guarantees — creates false confidence.
- Overly broad; Copilot can still safely assist with non-crypto parts of the same project (docs, boilerplate, tests).

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A production bug occurs intermittently only under high concurrent load. A developer pastes the function into Copilot Chat and asks for a fix. What is the key limitation of Copilot in this scenario?

A) Copilot has no access to runtime state, logs, or execution history, so it can only reason from the static code provided
B) Copilot cannot suggest any code changes for concurrency bugs
C) Copilot will refuse to answer questions about bugs
D) Copilot requires elevated GitHub permissions to analyze runtime bugs

<details>
<summary>Answer</summary>

**Correct: A**

Correct limitation — no visibility into logs or runtime timing means suggestions are based only on the code/text shown, often insufficient for concurrency issues.

**Why the others are wrong:**
- Copilot can still propose plausible fixes, just without certainty tied to actual runtime behavior.
- Copilot doesn't refuse; it may just give lower-confidence answers.
- No such permission requirement exists for reasoning about pasted code.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A developer wants to convert utility functions written in Java to equivalent TypeScript. Which Copilot capability is designed for this task?

A) Copilot Chat, by directly asking it to translate the code to the target language
B) Copilot inline autocomplete suggestions only
C) The /doc slash command
D) GitHub Copilot Voice

<details>
<summary>Answer</summary>

**Correct: A**

There is no dedicated translation slash command — Copilot Chat handles cross-language translation when asked conversationally.

**Why the others are wrong:**
- Inline autocomplete completes code as typed; not designed for whole-file translation requests.
- /doc generates documentation comments, not language translation.
- Copilot Voice is a dictation/accessibility input method, not a translation capability.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which Copilot Chat slash command is used to generate unit tests for a selected function?

A) /doc
B) /explain
C) /simplify
D) /tests

<details>
<summary>Answer</summary>

**Correct: D**

/tests is the built-in command specifically for generating test cases for selected code.

**Why the others are wrong:**
- /doc generates documentation comments, not tests.
- /explain describes what code does; it does not generate tests.
- /simplify proposes a simplified version of code, unrelated to test generation.

</details>

---

**Q6.** In VS Code, where does a developer trigger Copilot to auto-generate a commit message based on staged changes?

A) By typing /commit in the integrated terminal
B) By running a Copilot commit command in GitHub CLI
C) Commit message generation is only available in GitHub.com's web editor
D) By clicking the sparkle/Copilot icon in the Source Control panel's commit message box

<details>
<summary>Answer</summary>

**Correct: D**

VS Code's Source Control view has a Copilot-generated commit message action that summarizes staged diffs into a suggested message.

**Why the others are wrong:**
- No such terminal slash command exists for commit messages.
- The GitHub CLI's Copilot integration is for command suggestions/explanations, not diff-based commit messages in VS Code.
- The feature is available in supported IDEs like VS Code, not limited to the web editor.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which feature allows Copilot to automatically generate a pull request title and description summarizing the code changes?

A) Copilot Autocomplete
B) Copilot for Pull Requests (PR summary generation)
C) Copilot in the CLI
D) Copilot Extensions API

<details>
<summary>Answer</summary>

**Correct: B**

Copilot's PR summary feature reads the diff and generates a descriptive title and summary for the pull request.

**Why the others are wrong:**
- Autocomplete only completes code as you type, not PR text.
- CLI Copilot explains/suggests terminal commands, unrelated to PR descriptions.
- The Extensions API is for building custom Copilot integrations, not a built-in PR summary generator.

</details>

---

**Q8.** What is the key difference between Copilot's 'explain' capability and its 'refactor' capability on a block of code?

A) Explain rewrites the code to improve performance; refactor only adds comments
B) Explain describes what the existing code does without changing it; refactor proposes a restructured version while preserving behavior
C) They are the same feature with different names
D) Explain only works on entire files, refactor only works on single lines

<details>
<summary>Answer</summary>

**Correct: B**

This is the core distinction: explain = understanding with no code changes; refactor = code transformation with preserved behavior.

**Why the others are wrong:**
- This reverses the actual definitions of the two capabilities.
- They are distinct capabilities with different purposes and outputs.
- No such scope restriction exists; both can apply to selections or whole files.

</details>

---

