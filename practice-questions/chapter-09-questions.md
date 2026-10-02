## Chapter 9: Testing with GitHub Copilot — Practice Questions

**Q1.** A developer runs /tests on a function that validates email format. Copilot generates three tests, all using valid email strings. What should the developer do before merging?

A) Merge immediately since all generated tests pass
B) Re-run /tests with no changes until it produces more tests
C) Disable Copilot test generation for this file
D) Manually add tests for invalid formats, empty strings, and boundary-length inputs that Copilot missed

<details>
<summary>Answer</summary>

**Correct: D**

Copilot's /tests output commonly covers only the 'happy path'. The developer must identify the coverage gap and manually add edge cases and boundary/invalid inputs.

**Why the others are wrong:**
- Passing tests only prove the happy path works, not that edge cases are handled
- Re-running the same command without new guidance rarely produces different coverage
- Disabling the feature abandons a useful starting point instead of fixing the gap

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A team merged Copilot-generated tests without review. Later, a bug shipped because the tests passed regardless of the function's actual output. What is the root cause?

A) A bug in the /tests slash command itself
B) The CI pipeline was misconfigured to skip test execution
C) The generated tests lacked meaningful assertions and were never validated before merge
D) Copilot Chat crashed during generation

<details>
<summary>Answer</summary>

**Correct: C**

AI-generated tests can be structurally valid but assert nothing meaningful (false positives). Human review before merge is required to catch missing/weak assertions.

**Why the others are wrong:**
- The scenario describes a review-process failure, not a tool defect
- Nothing in the scenario indicates CI configuration issues
- The tests ran and passed, so there was no crash

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** Using /tests on a discount-calculation function with quantity tiers (0-9, 10-49, 50+), Copilot generates tests for only the 0-9 tier. What is the best next step?

A) Merge the tests and file a ticket to add coverage later
B) Prompt Copilot explicitly to generate tests covering the boundary values between each tier
C) Rewrite the entire discount function from scratch
D) Switch to a different code editor

<details>
<summary>Answer</summary>

**Correct: B**

Giving Copilot more specific context/instructions (e.g., 'generate tests at tier boundaries 9/10 and 49/50') is the recommended way to close AI-generated coverage gaps.

**Why the others are wrong:**
- Deferring boundary coverage risks shipping untested logic errors at tier transitions
- Rewriting the function does not address the missing test coverage
- The editor is unrelated to the coverage gap

</details>

---

**Q4.** Which GitHub Copilot capability is specifically designed to generate unit tests for selected code directly in the editor or chat?

A) Copilot Autofix
B) The /tests slash command in Copilot Chat
C) Copilot code review
D) Copilot Workspace

<details>
<summary>Answer</summary>

**Correct: B**

/tests is the slash command purpose-built to generate unit tests for the selected code or open file context.

**Why the others are wrong:**
- Copilot Autofix targets fixing flagged security/code-scanning issues, not generating tests
- Copilot code review provides review comments on pull requests, not test generation
- Copilot Workspace is for planning and implementing multi-file changes, not a dedicated test generator

</details>

---

**Q5.** A developer wants Copilot to produce realistic mock fixture data for a test suite involving User objects. Which approach is most appropriate?

A) Hardcode all fixtures manually without any Copilot assistance
B) Only use /tests and ignore fixture generation entirely
C) Use Copilot Autofix to create the fixtures
D) Ask Copilot Chat to generate fixture data that matches the existing type/schema definitions

<details>
<summary>Answer</summary>

**Correct: D**

Copilot Chat can generate realistic, schema-consistent test data and fixtures when given the relevant type definitions as context.

**Why the others are wrong:**
- Manual-only fixture creation ignores a productive use case for Copilot
- /tests generates test cases, not necessarily comprehensive fixture data on its own
- Autofix is for remediating flagged issues, not generating test data

</details>

---

**Q6.** When invoking /tests in Copilot Chat, what primarily determines the scope of code Copilot analyzes to generate tests?

A) The currently selected code or the open file's context
B) The entire repository is scanned automatically
C) Only the most recently committed file
D) A configuration file named copilot-tests.yml

<details>
<summary>Answer</summary>

**Correct: A**

/tests operates on the code currently selected or in context in the editor/chat, not the whole repo.

**Why the others are wrong:**
- Copilot does not scan the entire repository for a single /tests invocation
- Scope is based on current selection/context, not commit history
- No such configuration file governs /tests scope

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** Which practice best mitigates the risk of merging AI-generated tests that contain missing or weak assertions?

A) Trusting Copilot's output without additional review
B) Increasing the raw number of generated tests automatically
C) Disabling code coverage tooling to avoid false confidence
D) Requiring human code review of generated tests before merge, verifying that assertions are present and meaningful

<details>
<summary>Answer</summary>

**Correct: D**

Human review is the mandatory safeguard against AI-generated tests that look correct but fail to validate real behavior.

**Why the others are wrong:**
- Blind trust is exactly the practice that leads to false positives reaching production
- More tests without meaningful assertions does not reduce risk
- Disabling coverage tooling removes a useful signal rather than fixing the underlying issue

</details>

---

**Q8.** What is a key limitation of tests generated by Copilot's /tests command?

A) They can automatically execute in production environments
B) They always achieve 100% code coverage automatically
C) They may pass without truly validating behavior, due to missing or weak assertions (false positives)
D) They completely replace the need for human-written tests

<details>
<summary>Answer</summary>

**Correct: C**

A well-documented limitation is that generated tests can be structurally valid yet fail to assert meaningful behavior, creating false confidence.

**Why the others are wrong:**
- Copilot does not execute tests in production; it only generates test code
- Generated tests frequently leave coverage gaps, especially for edge cases
- Generated tests are a starting point requiring human review, not a full replacement

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

