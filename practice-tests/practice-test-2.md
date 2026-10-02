# Practice Test 2: GH-300: GitHub Copilot Certification Exam Prep

- **Questions:** 47
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-2.md`. Track results in `score-tracker.md`.

---

**Q1.** A financial services company wants developers to ask Copilot Chat questions directly on GitHub.com and receive answers grounded in a curated set of internal README files and architecture docs from specific repositories. Which capability, and minimum plan, satisfies this requirement?

A) Copilot Business, using the default chat context from the currently open repository
B) Copilot Individual (Pro), using the .github/copilot-instructions.md file
C) Copilot Enterprise, using a custom knowledge base built from the selected repositories
D) Copilot Extensions installed on Copilot Business to index the documentation repos

---

**Q2.** A backend engineer wants to get an explanation of a complex shell one-liner and generate a new git command, entirely from the terminal without switching to an editor or browser. Which Copilot feature should they use?

A) GitHub Copilot in the CLI (gh copilot explain / suggest)
B) GitHub Copilot inline chat in the IDE
C) GitHub Copilot code review on the pull request
D) GitHub Copilot Extensions in GitHub.com

---

**Q3.** An organization's legal team requires that Copilot never surface suggestions that closely match public code longer than a small number of characters, across every repository in the org. Where should an organization owner configure this?

A) In each repository's .github/copilot-instructions.md file
B) In the organization's Copilot policy settings, by setting 'Suggestions matching public code' to Block
C) In each developer's personal IDE Copilot extension settings
D) In the repository's content exclusion (copilot-exclusions) configuration

---

**Q4.** A team lead at a company with GitHub Copilot Business wants developers to install a third-party Copilot Extension so they can query an internal ticketing system directly from Copilot Chat. What must happen first at the organization level?

A) The organization must upgrade to Copilot Enterprise, since Extensions require Enterprise
B) An org admin must enable the Copilot Extensions policy in organization settings
C) Each developer must generate a personal access token and add it to copilot-instructions.md
D) Nothing — Extensions install automatically once the org has any paid Copilot plan

---

**Q5.** A solo open-source maintainer only has a free personal GitHub account and wants some Copilot code completion and chat capability without paying. What is a key limitation of GitHub Copilot Free compared to Copilot Individual (Pro)?

A) Copilot Free includes organization-managed knowledge bases that Pro lacks
B) Copilot Free is only available to Enterprise Managed User accounts
C) Copilot Free requires an organization to assign the user a seat
D) Copilot Free is capped at roughly 2,000 completions and 50 chat interactions per month, while Pro is unlimited

---

**Q6.** An enterprise administrator wants to enable Copilot in the CLI for only the 'Platform' team while keeping it disabled for every other Copilot user in the same organization. What is the correct approach?

A) Configure a team-level allow-list for the CLI policy in organization settings
B) Enable the 'Copilot in the CLI' organization policy, understanding it applies to all Copilot-seated users — GitHub does not support scoping this policy to a single team
C) Assign the Platform team a separate 'CLI-enabled' Copilot license type
D) Add a copilot-cli.yml file to the Platform team's repositories to scope access

---

**Q7.** A GitHub Enterprise Cloud customer wants developers to ask Copilot Chat questions about internal architecture decisions and have Copilot Chat answer using indexed content from a curated set of private repositories, without developers manually pasting in documentation. Which capability should the admin configure?

A) Enable content exclusion on the documentation repositories
B) Upgrade all developers to Copilot Pro+ for a larger context window
C) Create a Copilot knowledge base referencing those repositories
D) Install a Copilot Extension that links to an internal wiki tool

---

**Q8.** An organization owner wants to enforce, across the entire organization, that Copilot never returns a suggestion matching a public code snippet above the built-in matching threshold. Where must this be configured?

A) In the organization's Copilot policy setting 'Suggestions matching public code', set to Blocked
B) In each developer's personal Copilot settings on github.com
C) In the repository's branch protection rules
D) In a .gitignore file at the root of every repository

---

**Q9.** A development team wants to type natural-language commands inside Copilot Chat in their IDE to create, comment on, and transition issues in a third-party tool like Jira, without leaving the editor. Which Copilot capability enables this kind of integration with an external service?

A) Copilot code review
B) Built-in slash commands in Copilot Chat
C) Copilot Extensions
D) Copilot knowledge bases

---

**Q10.** A developer wants an explanation of a complicated multi-pipe shell command and a suggested git command to recover from a bad rebase, entirely from their terminal, without switching to the IDE or browser. Which Copilot feature fits this need?

A) Copilot inline chat in the code editor
B) Copilot code review in pull requests
C) GitHub Copilot in the CLI (gh copilot explain / gh copilot suggest)
D) Copilot autocomplete in the IDE's integrated terminal pane

---

**Q11.** An individual, non-organization subscriber frequently exhausts their monthly allowance of premium requests when using advanced reasoning models for large refactors, and wants the highest premium-request allowance available to a single paying individual. Which plan should they choose?

A) Copilot Business
B) Copilot Free
C) Copilot Pro
D) Copilot Pro+

---

**Q12.** Which statement correctly distinguishes GitHub Copilot Enterprise from GitHub Copilot Business?

A) Only Copilot Business supports IDE code completions; Enterprise is chat-only
B) Copilot Enterprise adds capabilities like Copilot knowledge bases and deeper Copilot Chat integration across GitHub.com (such as in pull requests and code search) that Business does not include
C) Copilot Business supports fine-tuned/knowledge-base-grounded models, while Enterprise does not
D) Only Copilot Enterprise allows assigning seats to individual organization members

---

**Q13.** An organization on GitHub Copilot Business wants to guarantee that a specific internal repository containing cryptographic keys is never used as contextual input for Copilot code completions or Copilot Chat, while still allowing engineers to browse the repository normally on GitHub. Which configuration should the organization apply?

A) Remove all engineers' Copilot seats whenever they work in that repository
B) Enable the 'Suggestions matching public code' blocking policy
C) Create a Copilot Extension that filters sensitive files before indexing
D) Configure a content exclusion rule for the repository in the organization's Copilot settings

---

**Q14.** A platform team wants developers to invoke their internal deployment-status service directly from Copilot Chat in the IDE using a custom slash command, with authentication handled through the company's existing GitHub App. Which Copilot capability should the team build?

A) A Copilot knowledge base pointing to the deployment service's documentation
B) A custom alias in Copilot in the CLI
C) A Copilot Extension built on the GitHub Apps platform
D) An organization-level content exclusion rule referencing the deployment service

---

**Q15.** A security team at ExampleCorp, which uses GitHub Copilot Business, asks whether the proprietary source code their developers write while using Copilot could end up being used to train the underlying AI model for other customers. Which statement correctly describes GitHub's policy?

A) GitHub Copilot Business and Enterprise do not use customers' code snippets, prompts, or suggestions to train the underlying LLMs; this differs from the default telemetry behavior available on personal Copilot Free/Pro accounts.
B) GitHub Copilot Business retains all code snippets indefinitely and periodically fine-tunes the shared model using customer code from every plan tier.
C) Copilot only avoids training on code if the repository is private; public repository code accessed by Copilot is always eligible for model training regardless of plan.
D) Training exclusion applies only when the organization enables the 'Block public code matching' policy, and model training on customer code is otherwise on by default for all plans.

---

**Q16.** Which of the following best describes how GitHub Copilot assembles the context it sends to the language model when generating an inline code completion in the editor?

A) It sends only the single line where the cursor is located, without any surrounding code.
B) It transmits the entire contents of every file in the repository to give the model full project awareness.
C) It sends solely the docstring or comment immediately preceding the cursor, ignoring any actual code.
D) It builds a prompt containing the code before and after the cursor in the current file, plus relevant snippets from other open tabs/related files, then sends that contextual prompt to the model.

---

**Q17.** An organization owner is configuring Copilot Business policies and sets the 'Suggestions matching public code' policy to Block. What effect does this have on Copilot's suggestion flow?

A) Copilot stops generating suggestions entirely for any file that has ever contained public code.
B) Matching suggestions are still shown to developers but flagged with a warning banner in the editor for manual review.
C) The setting only affects Copilot Chat responses and has no effect on inline code completions.
D) The backend filtering layer compares generated suggestions against public code on GitHub and suppresses any suggestion (roughly 150 characters or longer) that matches, so the matching suggestion is never returned to the editor.

---

**Q18.** Developers at a Copilot Enterprise organization want Copilot Chat on GitHub.com to answer questions that reference internal documentation and code across multiple repositories, not just the file currently open. Which Copilot Enterprise capability enables this?

A) Content exclusion rules, which broaden Copilot's visibility to any repository once enabled.
B) The public code matching filter, which indexes GitHub.com's public repositories for enterprise search.
C) Copilot Enterprise knowledge bases, which use semantic indexing of selected internal repositories so Chat can retrieve relevant context beyond the open file.
D) Neighboring tabs context, which is automatically extended to include every repository in the organization.

---

**Q19.** Which statement most accurately reflects the underlying large language models (LLMs) that power GitHub Copilot as of 2026?

A) Copilot supports multiple LLMs from different providers (for example, OpenAI and Anthropic models), and supported plans/IDEs let users or admins choose among available models for Copilot Chat, while completions use an optimized default model.
B) Copilot exclusively runs a single proprietary GitHub-trained model called Codex, with no alternative models available on any plan.
C) Copilot relies solely on open-source community models that customers must self-host to use Copilot Chat.
D) All Copilot suggestions, whether Chat or inline completions, are generated by fine-tuning a separate model per customer organization using that organization's private code.

---

**Q20.** A Copilot Business admin configures a content exclusion rule for the path secrets/** across the organization's repositories. A developer opens a file under that path in their editor. What is the expected behavior?

A) Copilot treats the excluded file as invisible: its content is not sent as context, no completions are offered inside it, and the exclusion applies consistently across the organization wherever the policy is enforced.
B) Content exclusion only prevents the file from appearing in Copilot Chat's 'attach file' picker; the file's content can still be used silently as background context for completions elsewhere.
C) Copilot Chat is disabled organization-wide, but inline completions still work normally inside the excluded path.
D) Copilot will not use the file's contents as context for suggestions and will not offer inline completions while that file is active, but the exclusion only applies within that specific IDE session.

---

**Q21.** An enterprise administrator enables the 'Suggestions matching public code' filter for their organization in GitHub Copilot Business. A developer receives a suggestion that closely matches a public GitHub repository. What happens to that suggestion?

A) It is automatically flagged for legal review and the developer is notified via email
B) The suggestion is blocked from being shown or automatically filtered out entirely so it never reaches the developer
C) The suggestion is shown but appended with a license disclaimer comment for the developer to review
D) The suggestion is shown alongside a link to the matching public repository so the developer can verify the license

---

**Q22.** A company using GitHub Copilot Business wants to understand exactly what happens to code snippets sent as context when a developer requests a suggestion. Which statement correctly describes this data flow for Business/Enterprise plans?

A) All context sent to Copilot is permanently stored in the developer's organization audit log for compliance purposes
B) Copilot never transmits file content off the developer's machine; suggestions are generated entirely by a local model
C) Prompts are sent to the Copilot service and are used to fine-tune a private model exclusively for that organization within 24 hours
D) Prompts and context snippets are sent to the Copilot service to generate a suggestion, but for Business and Enterprise plans this data is not retained for training GitHub's underlying models

---

**Q23.** A developer working in a large enterprise repository asks Copilot Chat a question referencing a function defined in another file within the same repository. Under Copilot Enterprise's codebase indexing feature, how does Copilot most likely locate and use that relevant context?

A) It requires the developer to manually paste the entire other file into the chat prompt every time
B) It relies solely on the currently open file and nearby tabs, with no awareness of other files in the repository
C) It performs a live full-text scan of every file in the remote repository at the moment of each request
D) It uses a pre-built semantic index of the repository to retrieve relevant code snippets and includes them as additional context automatically

---

**Q24.** An organization owner configures a content exclusion rule at the organization level that excludes all files matching `**/vendor/**` from Copilot's context across every repository. A repository administrator in one specific repo wants Copilot to see files in that repo's `vendor/` folder because they contain internally maintained code, and creates a repo-level rule attempting to re-include them. What actually happens?

A) The repo admin can create a repo-level exclusion rule with a negation pattern to override the org rule
B) The most restrictive rule wins — the repo admin cannot re-enable Copilot access to files the organization has excluded
C) Repo-level settings always take precedence over organization-level settings
D) Content exclusions only apply to Copilot Chat, so code completions will still see the vendor folder regardless

---

**Q25.** Where must repository-level Copilot content exclusion rules be defined for GitHub Copilot Business or Enterprise?

A) In a `.copilotignore` file at the repository root, using `.gitignore`-style syntax
B) In the organization's `SECURITY.md` file using YAML front matter
C) In a `copilot-exclusions.json` file stored inside the `.vscode` folder
D) In the repository's `.github/copilot.yml` file, under a key that lists excluded glob patterns

---

**Q26.** A GitHub Copilot Business administrator wants to guarantee that no developer in the organization can disable the filter that blocks suggestions matching publicly available code. What should the administrator do, and how does this compare to Copilot Individual?

A) The admin can enforce the public-code-matching block as an organization-wide policy in Business/Enterprise settings, locking it for all members; Copilot Individual users can only toggle this setting for themselves
B) This setting can only be controlled per-developer in both plans; org admins have no policy control over it
C) The filter is hard-coded to always be on in every Copilot plan and cannot be disabled by anyone
D) The filter only affects Copilot Chat responses, not inline code suggestions, so it cannot be enforced organization-wide

---

**Q27.** A company evaluating Copilot Business is concerned about intellectual property risk from suggestions that might reproduce public code verbatim. Which statement correctly describes GitHub's Copilot IP indemnification commitment?

A) GitHub indemnifies IP claims for Copilot-generated code equally across Individual, Business, and Enterprise plans
B) IP indemnification only applies if the customer disables the public-code-matching filter entirely, since that increases coverage
C) GitHub offers an IP indemnity commitment to Copilot Business and Enterprise customers, contingent on the customer having the public-code-matching (duplication detection) filter enabled
D) GitHub provides no IP indemnification for any Copilot plan; customers must obtain separate third-party insurance

---

**Q28.** How do GitHub Copilot Individual and Copilot Business/Enterprise differ regarding whether a developer's code is used to train GitHub's underlying models?

A) Both plans use submitted code snippets for training by default with no way to opt out
B) Copilot Business and Enterprise use customer code for training by default, while Individual users are fully excluded from any data use
C) Copilot Individual users may have their code used to help improve/train models unless they opt out in personal settings; Copilot Business and Enterprise customer data (prompts, suggestions, code) is not used to train GitHub's models
D) Neither plan ever uses customer code for any purpose whatsoever, including abuse monitoring or debugging

---

**Q29.** A developer working in a repository with a content exclusion configured for `config/secrets.yaml` asks Copilot Chat, "Summarize the contents of config/secrets.yaml." What should happen?

A) Copilot Chat will summarize the file because content exclusions only apply to inline code completions, not chat
B) Copilot Chat will not use the excluded file as context and will indicate it cannot access that file's contents, since exclusions apply to both completions and chat
C) Copilot Chat will refuse to answer any question at all and disable itself for the rest of the session
D) Copilot Chat will summarize the file but automatically redact any strings that look like secrets using pattern matching

---

**Q30.** An organization on GitHub Copilot Business has enabled a content exclusion rule for the path '/legacy/**' in one repository. A developer opens a file inside '/legacy/' in their editor but also has an unrelated repository open in the same workspace without any exclusion configured. What is the correct behavior of Copilot in this scenario?

A) Copilot disables all suggestions across the entire workspace because one repository has an active exclusion rule
B) Copilot will not use the excluded file's content as context, but suggestions in the other repository's files continue to work normally based on their own context
C) Copilot suggestions are disabled only for the excluded file, but the excluded file's content can still be used as context for suggestions in other open files
D) Content exclusions only apply to the Copilot Chat panel, so inline completions still use the excluded file as context

---

**Q31.** A developer joins a project and must modify a 300-line function in an unfamiliar legacy module with zero comments before making a bug fix. Which Copilot workflow BEST prepares them to safely modify the code?

A) Read the raw code line by line without Copilot assistance to build full mental context
B) Let inline ghost-text completions continue the function so Copilot reveals its intended behavior
C) Ask Copilot CLI in the terminal to explain the file path and directory structure
D) Select the function and use the /explain command in Copilot Chat to get a plain-language breakdown before editing

---

**Q32.** A team wants pull requests opened on GitHub.com to automatically get an AI-generated summary of the code changes to speed up review, without anyone leaving the PR page. Which Copilot capability should they use?

A) The Copilot-generated PR summary feature available directly in the GitHub.com pull request creation view
B) Copilot code completion inside the IDE while writing the feature branch code
C) Copilot CLI's `gh copilot suggest` command run locally before pushing
D) Manually asking Copilot Chat in the IDE to draft a commit message for each commit

---

**Q33.** A developer selects a function and runs the /tests command in Copilot Chat, but the generated unit tests are shallow and miss key edge cases the function actually handles. What is the MOST effective next step?

A) Add descriptive comments about expected inputs/edge cases and open related test files for context, then re-run /tests
B) Increase the IDE's suggestion delay setting so Copilot has more time to think
C) Upgrade the organization from Copilot Business to Copilot Enterprise to get better test generation
D) Abandon Copilot and write all tests manually since AI test generation is unreliable

---

**Q34.** In Copilot Chat, which slash command is specifically designed to generate unit tests for the currently selected code?

A) /fix
B) /explain
C) /tests
D) /doc

---

**Q35.** A developer needs to port an entire Python data-processing script to idiomatic TypeScript, preserving business logic and naming conventions of the target ecosystem. Which approach gives the MOST reliable result?

A) Use inline ghost-text completions to translate the script function-by-function without opening the full file
B) Rely solely on Copilot CLI to generate the translated file from the command line
C) Paste snippets of the code into the review comment box of a Copilot-reviewed pull request and accept its suggestions
D) Open the Python file, use Copilot Chat, explicitly state the target language and desired conventions, ask it to translate the whole file, then review and test the output

---

**Q36.** Which of the following is the LEAST appropriate use case for accepting a Copilot suggestion without rigorous independent review by a subject-matter expert?

A) Generating boilerplate CRUD REST endpoints for a standard resource
B) Implementing a custom cryptographic encryption algorithm for a security-critical system
C) Writing docstrings for well-defined, already-tested utility functions
D) Suggesting variable names during a routine refactor

---

**Q37.** A developer is working in a large monorepo using Copilot Chat in VS Code. Before refactoring a function called `calculateShippingCost`, they need Copilot to identify every file in the repository that calls this function and explain how it is used in each context. Which approach BEST accomplishes this?

A) Use the @workspace participant and ask 'Where is calculateShippingCost used across this project, and how?'
B) Highlight the function definition and use inline chat to ask 'refactor this'
C) Run the /explain slash command on the function definition only
D) Manually open every file in the repo and paste their contents into a single chat message

---

**Q38.** A developer is using GitHub Copilot Chat on github.com and wants to ask a question about why a GitHub Actions workflow run failed, referencing the actual run logs and repository configuration. Which chat participant is the BEST fit for this task?

A) @terminal
B) @vscode
C) @github
D) @workspace

---

**Q39.** In VS Code, a developer wants Copilot Chat to base its answer strictly on the contents of one specific file, `utils.py`, rather than pulling in other open files or the whole workspace. Which prompt syntax achieves this?

A) /file utils.py
B) #file:utils.py
C) @workspace utils.py
D) $utils.py

---

**Q40.** A developer wants Copilot Chat to generate new API endpoint handlers that follow the exact same structure, naming conventions, and error-handling style as three existing handlers already in the codebase. Which prompting technique BEST achieves this?

A) Zero-shot prompting: simply ask 'write a new endpoint handler' with no examples
B) Few-shot prompting: include the three existing handlers as examples in the prompt/context, then ask for a new one following the same pattern
C) Iterative prompting: submit the same request repeatedly until the output happens to match the style
D) Slash-command chaining: run /fix followed by /tests on an empty file

---

**Q41.** A developer asks GitHub Copilot Chat to generate unit tests for a payment-processing function that must handle currency rounding, null inputs, and negative amounts. The initial generated tests only cover the happy path. What is the BEST next step?

A) Prompt Copilot explicitly to add edge-case tests for null inputs, negative amounts, and rounding boundaries, then manually review the assertions
B) Accept the generated tests as final since Copilot already analyzed the function
C) Disable Copilot for this file and write all tests manually from scratch
D) Ask Copilot to raise code coverage to 100% without specifying which scenarios to cover

---

**Q42.** A team notices several Copilot-generated unit tests pass immediately after creation but do not fail when a bug is intentionally introduced into the corresponding source code. What does this most likely indicate, and what should the team do?

A) The test framework is misconfigured and must be reinstalled before rerunning Copilot
B) This proves the source code is already bug-free and no further action is needed
C) Copilot cannot generate valid tests under any circumstances and should be disabled for the project
D) The tests likely contain weak or tautological assertions that don't validate real behavior, so developers must review and strengthen them

---

**Q43.** Which GitHub Copilot capability is specifically designed to generate unit tests for a selected function directly within the IDE via a dedicated command?

A) The /tests slash command in Copilot Chat
B) Copilot code review
C) Copilot Autofix
D) Copilot Chat's /explain command

---

**Q44.** A repository contains existing test files written with pytest, using fixtures and parametrized test functions. When a developer asks Copilot to generate a new test for an untested function in the same repository without specifying a framework, what will most strongly influence which testing framework and style Copilot uses?

A) Copilot always defaults to the most popular testing framework globally regardless of repository content
B) Copilot randomly selects a framework from a fixed internal list each time
C) The existing code and context in the repository, such as current test files, imports, and conventions already present
D) Copilot ignores existing repository files and only uses the language's official default test library

---

**Q45.** A GitHub Enterprise Cloud organization enables the 'Block suggestions matching public code' policy for Copilot Business. A developer later receives a suggestion that closely resembles a snippet from a well-known open-source repository, but the suggestion is NOT blocked. What is the MOST likely explanation?

A) The filter matches only exact or near-exact code sequences; paraphrased or logically similar code may not be detected
B) The filter only scans public code stored in Microsoft-owned repositories, not third-party open-source projects
C) The policy must be re-enabled locally by each individual developer even after an org admin turns it on
D) The filter only applies to Copilot Chat responses, not inline code completions

---

**Q46.** A developer accepts a Copilot-generated function that introduces a SQL injection vulnerability, which is later discovered in production. According to GitHub's responsible-AI guidance for Copilot, who bears accountability for the shipped vulnerability?

A) GitHub, because Copilot is the tool that generated the insecure code
B) The developer and their team, because human review and validation of AI suggestions is required before acceptance
C) No one, because AI-assisted code is exempt from standard code review and testing policies
D) The organization's Copilot administrator, because they configured the content exclusion settings

---

**Q47.** A team lead is concerned that Copilot-generated code may reproduce license-restricted snippets (e.g., copyleft-licensed code) verbatim without attribution. Which Copilot Business/Enterprise feature is specifically designed to help mitigate this particular risk?

A) Copilot's automatic license classifier, which tags each suggestion with its source repository's license
B) The content exclusion (.copilotignore) configuration, which prevents any licensed files in the repo from being suggested
C) The public code matching filter, which can block suggestions that match public code (including license-restricted snippets)
D) Copilot Chat's explain-this-code command, which documents the original source of any generated function

---

