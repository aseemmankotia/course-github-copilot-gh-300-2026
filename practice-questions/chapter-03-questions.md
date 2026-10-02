## Chapter 3: Copilot in the CLI, GitHub.com, Pull Requests, and Extensions — Practice Questions

**Q1.** A developer is about to run a long, unfamiliar shell command they copied from a forum post and wants to know exactly what it does before executing it. Which GitHub Copilot CLI command should they use?

A) gh copilot suggest -t shell
B) gh copilot chat
C) gh copilot explain
D) gh copilot review

<details>
<summary>Answer</summary>

**Correct: C**

gh copilot explain takes an existing command as input and returns a plain-language breakdown of what each part does — exactly the use case of understanding an unfamiliar command before running it.

**Why the others are wrong:**
- gh copilot suggest generates a new command from a natural-language description; it does not explain an existing one.
- gh copilot chat is not a real CLI subcommand — Copilot Chat is a separate surface (IDE, GitHub.com, Mobile), not part of the gh-copilot extension's command set.
- gh copilot review does not exist; code review is invoked through the GitHub.com pull request UI, not the CLI extension.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer wants Copilot CLI to generate a git command to undo the last commit but keep the changes staged, using natural language input in the terminal. Which command and target should they use?

A) gh copilot suggest -t git
B) gh copilot explain -t git
C) gh copilot suggest -t shell
D) gh copilot suggest -t gh

<details>
<summary>Answer</summary>

**Correct: A**

gh copilot suggest -t git generates git-specific commands from a natural-language description, matching the requirement to undo a commit while keeping changes staged.

**Why the others are wrong:**
- explain is for interpreting existing commands, not generating new ones.
- -t shell targets general shell commands, not git-specific operations; while it may still work, git is the correct, more specific target for this scenario.
- -t gh targets GitHub CLI (gh) commands, not native git commands.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An enterprise wants Copilot Chat on GitHub.com to answer developer questions by referencing content from the organization's internal architecture documentation stored in private repositories. What must be configured first?

A) Enable Copilot code review for all repositories
B) Create a knowledge base by indexing the relevant repositories (requires Copilot Enterprise)
C) Assign every developer a Copilot Business seat
D) Install a Copilot Extension that links to the documentation repos

<details>
<summary>Answer</summary>

**Correct: B**

Knowledge bases let Copilot Chat reference the content of specific repositories, but the repositories must first be indexed into a knowledge base, and this feature is only available on GitHub Copilot Enterprise.

**Why the others are wrong:**
- Code review is unrelated to chat referencing documentation — it reviews pull request diffs, not general knowledge queries.
- Copilot Business does not include knowledge bases; the feature requires Enterprise regardless of seat count.
- Copilot Extensions integrate external tools/services via chat skillsets; they are not the mechanism for indexing internal repo documentation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q4.** A team wants Copilot to automatically draft a description of the code changes whenever a pull request is opened. Which feature provides this?

A) Copilot knowledge bases
B) Copilot pull request summaries
C) Copilot Extensions
D) gh copilot explain

<details>
<summary>Answer</summary>

**Correct: B**

Copilot pull request summaries automatically generate a natural-language description of the diff when a PR is opened, using the 'Ask Copilot' feature on GitHub.com.

**Why the others are wrong:**
- Knowledge bases power chat answers about indexed repo content, not PR descriptions.
- Copilot Extensions bring third-party tool integrations into chat, unrelated to auto-generating PR text.
- gh copilot explain interprets shell/CLI commands, not pull request diffs.

</details>

---

**Q5.** A company wants to bring their third-party incident-management tool into Copilot Chat so developers can type '@incident-tool' to query open incidents directly from GitHub.com. Which capability enables this?

A) Copilot knowledge base
B) Copilot Extension
C) Copilot code review
D) gh copilot suggest

<details>
<summary>Answer</summary>

**Correct: B**

Copilot Extensions let third-party services integrate with Copilot Chat as invokable agents (via @mention), bringing external tool data and actions directly into the chat experience.

**Why the others are wrong:**
- Knowledge bases only index GitHub repository content, not external third-party tool data.
- Code review is scoped to reviewing pull request diffs, not chat integrations with external tools.
- gh copilot suggest is a terminal command generator with no relation to chat integrations or third-party tools.

</details>

---

**Q6.** A developer wants to start using GitHub Copilot in their terminal to get command suggestions. What is the correct first step?

A) Enable Copilot code review in repository settings
B) Create a knowledge base and add the terminal repo
C) Install the Copilot Extension for the terminal
D) Run gh extension install github/gh-copilot

<details>
<summary>Answer</summary>

**Correct: D**

GitHub Copilot in the CLI is delivered as an extension to the GitHub CLI (gh), installed via gh extension install github/gh-copilot, after which suggest and explain subcommands become available.

**Why the others are wrong:**
- Code review settings are unrelated to enabling CLI functionality.
- Knowledge bases are for indexing repository documentation for chat, not for enabling terminal command suggestions.
- There is no dedicated 'terminal' Copilot Extension for this purpose — the CLI functionality comes from the gh-copilot extension itself.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** An organization owner is setting up a Copilot knowledge base so Chat can answer questions about their internal onboarding docs. Which prerequisite must be met?

A) All developers must have Copilot Individual seats
B) The organization must be on GitHub Copilot Enterprise and the target repositories must be indexed
C) Copilot Extensions must be enabled organization-wide
D) The repositories must be public

<details>
<summary>Answer</summary>

**Correct: B**

Knowledge bases require GitHub Copilot Enterprise, and the repositories containing the relevant content must be explicitly indexed before Chat can reference them.

**Why the others are wrong:**
- Copilot Individual seats are for personal accounts, not compatible with organization-level Enterprise-only features like knowledge bases.
- Copilot Extensions are a separate, independent feature and are not a prerequisite for knowledge bases.
- Repositories used in a knowledge base do not need to be public — private repos are supported and commonly used for internal documentation.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the fundamental difference between gh copilot suggest and gh copilot explain?

A) suggest reviews pull requests; explain reviews commits
B) suggest works only with git; explain works only with shell
C) suggest and explain are aliases for the same underlying function
D) suggest generates a new command from a natural-language description; explain interprets an existing command

<details>
<summary>Answer</summary>

**Correct: D**

suggest takes a natural-language description and outputs a command to run; explain takes an existing command and outputs a plain-language description of its behavior — they are inverse operations.

**Why the others are wrong:**
- Neither command reviews pull requests or commits — that functionality belongs to Copilot code review on GitHub.com.
- Both suggest and explain can target shell, git, or gh commands via the -t flag; neither is restricted to a single target type.
- They are distinct commands with opposite input/output directions, not aliases.

</details>

---

