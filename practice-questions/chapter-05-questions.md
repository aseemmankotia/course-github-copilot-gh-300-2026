## Chapter 5: How GitHub Copilot Works and Handles Data — Practice Questions

**Q1.** A developer on GitHub Copilot Business is worried that the private code they type will be used to train the underlying LLM. Which statement is accurate?

A) Business retains all prompts and uses them for training unless an admin opts out
B) Copilot Business and Enterprise do not use customer prompts or suggestions to train the underlying model
C) Only Copilot Individual excludes code from training, Business always includes it
D) Training use depends solely on the IDE extension, not the plan

<details>
<summary>Answer</summary>

**Correct: B**

GitHub's data handling terms state Business/Enterprise customer code (prompts and suggestions) is never used to train the underlying model.

**Why the others are wrong:**
- There is no opt-out needed — it's excluded by default for Business/Enterprise
- This reverses the actual distinction; Individual has an optional data-sharing setting, not Business
- The plan tier, not the IDE, governs this behavior

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** Which Copilot mechanism is responsible for detecting when a generated suggestion closely resembles existing public source code?

A) Content exclusion configuration
B) Matching public code (duplication detection) filter
C) Vulnerability prevention filter
D) Enterprise knowledge base indexing

<details>
<summary>Answer</summary>

**Correct: B**

The matching public code filter compares generated suggestions against public repositories to catch near-verbatim matches.

**Why the others are wrong:**
- Content exclusion controls what is sent as context, not output matching
- Vulnerability prevention targets insecure code patterns, not code provenance
- Knowledge base indexing provides retrieval context for chat, unrelated to duplication detection

</details>

---

**Q3.** An organization admin wants Copilot suggestions that match public code to be blocked entirely instead of shown with a citation. Where is this configured?

A) In each developer's personal IDE settings
B) In a .copilotignore file added to every repository
C) This behavior cannot be changed by an admin
D) In organization/enterprise Copilot policy settings under the 'suggestions matching public code' option

<details>
<summary>Answer</summary>

**Correct: D**

The block-vs-allow behavior for public code matches is an org/enterprise-level Copilot policy setting.

**Why the others are wrong:**
- Individual IDE settings do not control this org-wide security policy
- .copilotignore governs context exclusion, not output matching behavior
- This is a well-documented configurable admin policy

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A build-artifacts folder is listed in a repo's .gitignore but the organization has not configured Copilot content exclusion for that path. If a developer opens files from that folder, what happens?

A) .gitignore automatically excludes them from Copilot's context
B) They are excluded only for Copilot Individual users
C) Open files are always excluded from context regardless of ignore rules
D) They are used as context since .gitignore does not affect Copilot; only Copilot content exclusion rules do

<details>
<summary>Answer</summary>

**Correct: D**

.gitignore only governs git tracking; Copilot only respects its own content exclusion configuration (via org policy or .copilotignore) to omit paths from context.

**Why the others are wrong:**
- This is the exact trap the exam tests — .gitignore has no effect on Copilot context
- The plan tier does not change this behavior
- Open files are normally included as context by design

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which best describes the data retention difference between Copilot Business/Enterprise and Copilot Individual?

A) Individual never retains any data while Business/Enterprise retains everything permanently for training
B) Individual may allow prompts/suggestions to be used for product improvement if the user opts in, while Business/Enterprise exclude customer code from training by default and only retain data transiently for operational purposes like abuse detection
C) Both plans retain prompts identically with no configurable difference
D) Enterprise always shares customer code with third-party model vendors for training

<details>
<summary>Answer</summary>

**Correct: B**

This matches GitHub's published data handling model: Individual has an opt-in improvement setting; Business/Enterprise exclude code from training and retain data only briefly for safety/operations.

**Why the others are wrong:**
- Individual can still have short-term operational retention regardless of the training opt-in
- The plans are explicitly differentiated on this point — it's exam-relevant
- Business/Enterprise customer code is not used to train third-party vendor models

</details>

---

**Q6.** Which Copilot Enterprise feature allows Copilot Chat to answer questions using an organization's private repositories and documentation beyond the files currently open in the editor?

A) Content exclusion policy
B) Matching public code filter
C) Knowledge bases (semantic repository/document indexing)
D) Vulnerability prevention filter

<details>
<summary>Answer</summary>

**Correct: C**

Enterprise knowledge bases build a semantic index over selected repos/docs so Chat can retrieve relevant organizational context beyond the open editor context.

**Why the others are wrong:**
- Content exclusion restricts context, it doesn't add retrievable knowledge
- The public code filter concerns output matching, not internal knowledge retrieval
- Vulnerability prevention filters insecure code patterns, unrelated to retrieval

</details>

---

**Q7.** What is the primary purpose of Copilot's content filtering system that screens for toxicity and insecure code patterns?

A) To prevent offensive language and reduce suggestions containing known vulnerable coding patterns (e.g., hardcoded secrets, injection-prone code)
B) To detect and block suggestions matching public repositories
C) To index enterprise documentation for Copilot Chat
D) To determine which underlying LLM should service a request

<details>
<summary>Answer</summary>

**Correct: A**

Content filtering is a distinct safety layer covering offensive content and common security anti-patterns, separate from public code matching.

**Why the others are wrong:**
- That is the separate matching public code filter's job
- That describes Enterprise knowledge base indexing
- Model selection is handled by the model picker/backend routing, not content filtering

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** In a typical inline code-completion request, what context is sent to the Copilot backend to construct the prompt?

A) Only the single current line being typed
B) The entire repository's git commit history
C) Every file in the repository regardless of whether it is open
D) The current file content around the cursor plus snippets from neighboring open tabs, along with file path and language metadata

<details>
<summary>Answer</summary>

**Correct: D**

Copilot builds prompts from surrounding code in the active file plus related open tabs, along with metadata like path and language, to give the model relevant context.

**Why the others are wrong:**
- A single line provides insufficient context for useful completions
- Git history is not part of the inline completion prompt context
- Only open/relevant files contribute context, not the entire repo indiscriminately

</details>

---

