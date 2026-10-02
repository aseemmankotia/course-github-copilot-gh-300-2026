## Chapter 8: Prompt Crafting and Prompt Engineering for Copilot Chat — Practice Questions

**Q1.** A developer is inside Copilot Chat in VS Code and wants to find every file in the repository that references a deprecated `LegacyAuth` class, not just the currently open file. Which prompt syntax BEST accomplishes this?

A) "Find all references to LegacyAuth" with no open files
B) @github Find all references to LegacyAuth
C) @vscode Find all references to LegacyAuth
D) @workspace Find all references to LegacyAuth across the repository

<details>
<summary>Answer</summary>

**Correct: D**

@workspace indexes the entire opened project/repository, allowing Copilot Chat to search across files rather than being limited to the active editor tab.

**Why the others are wrong:**
- Without a participant, Copilot Chat only has context from open files/tabs, not the full repo index
- @github queries GitHub-hosted data like issues, PRs, and repo metadata via the GitHub extension, not local workspace code search
- @vscode answers questions about VS Code commands, settings, and extensions — not codebase content

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer wants Copilot Chat to tell them which VS Code keybinding toggles the integrated terminal. Which @-participant should they use?

A) @workspace
B) @github
C) @vscode
D) @terminal

<details>
<summary>Answer</summary>

**Correct: C**

@vscode is scoped to answer questions about the editor itself — commands, settings, and keybindings.

**Why the others are wrong:**
- @workspace is for questions about project source code, not editor configuration
- @github is for GitHub repository data such as issues and pull requests
- @terminal is not a supported Copilot Chat participant on the GH-300 exam objectives

</details>

---

**Q3.** Which slash command in Copilot Chat is used specifically to generate unit tests for the selected code?

A) /doc
B) /fix
C) /tests
D) /simplify

<details>
<summary>Answer</summary>

**Correct: C**

/tests instructs Copilot to generate unit test cases for the selected function or file.

**Why the others are wrong:**
- /doc generates documentation comments, not test code
- /fix proposes a fix for detected problems in the selected code
- /simplify rewrites code to be more concise, not to add tests

</details>

---

**Q4.** A developer asks Copilot Chat: "Write a function that validates an email address." This is an example of which prompting pattern?

A) Few-shot prompting
B) Iterative refinement
C) Zero-shot prompting
D) Context injection

<details>
<summary>Answer</summary>

**Correct: C**

Zero-shot prompting asks the model to complete a task with no examples provided — just a direct instruction.

**Why the others are wrong:**
- Few-shot prompting requires supplying one or more input/output examples in the prompt to steer format or behavior
- Iterative refinement refers to revising an existing response over multiple turns, not the initial request
- Context injection is not a standard term tested for this exam domain

</details>

---

**Q5.** A developer receives a Copilot Chat response that is close but uses the wrong logging library. What is the BEST next step per exam-recommended practice?

A) Reply in the same conversation specifying the correct logging library and asking Copilot to update the code accordingly
B) Start a brand new chat session and rephrase the entire request from scratch
C) Accept the response and manually rewrite the logging calls afterward
D) Switch to @github and ask it to fix the logging library choice

<details>
<summary>Answer</summary>

**Correct: A**

Iterative refinement means continuing the same conversational context with a specific follow-up correction, letting Copilot use prior context plus the new constraint.

**Why the others are wrong:**
- Starting a new session discards useful conversational context that already established the task
- Manually rewriting code bypasses using Copilot to correct its own output efficiently, which the exam expects as best practice
- @github is unrelated to fixing generated code logic; it is for GitHub repo metadata

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** A developer wants Copilot Chat to summarize open pull requests and their review comments for the current repository. Which participant provides this capability?

A) @workspace
B) @vscode
C) @github
D) No participant is needed since PR data is part of open files

<details>
<summary>Answer</summary>

**Correct: C**

@github connects Copilot Chat to GitHub-hosted data such as issues, pull requests, and discussions via the GitHub extension/API.

**Why the others are wrong:**
- @workspace only searches local project source files, not GitHub metadata like PRs
- @vscode is limited to editor commands and settings
- Pull request data is not part of local open files and requires explicit GitHub integration

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A developer has three files open in tabs but has not referenced any of them explicitly. They ask Copilot Chat a general coding question. What context does Copilot Chat use by default?

A) None — every prompt is answered with zero contextual awareness
B) The currently open/active editor tabs as available context
C) The entire repository, indexed automatically like @workspace
D) Only the file that was most recently saved to disk

<details>
<summary>Answer</summary>

**Correct: B**

Copilot Chat automatically considers content from currently open files/tabs as context even without an explicit @-participant, improving relevance of responses.

**Why the others are wrong:**
- Copilot Chat does use available open-file context by default; it is not context-blind
- Full repository indexing only occurs when @workspace is explicitly invoked
- Save state is irrelevant; open tab content is used regardless of save status

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which prompt below demonstrates few-shot prompting for generating commit messages in a specific format?

A) "Write a commit message for this change."
B) "Here are two examples of our commit format: 'feat: add login validation' and 'fix: resolve null pointer in parser'. Write a commit message in this format for the attached diff."
C) "@workspace write a commit message."
D) "/doc generate a commit message."

<details>
<summary>Answer</summary>

**Correct: B**

Providing labeled examples of the desired output format before the request is the defining trait of few-shot prompting.

**Why the others are wrong:**
- This is a bare zero-shot instruction with no examples given
- @workspace only adds repository context, it does not itself supply output examples
- /doc is a slash command for generating documentation comments, unrelated to commit message formatting or few-shot examples

</details>

---

