# Practice Test 1: GH-300: GitHub Copilot Certification Exam Prep

- **Questions:** 46
- **Time limit:** 90 minutes
- **Passing score:** 70%%

> Answers are in `answer-key-1.md`. Track results in `score-tracker.md`.

---

**Q1.** A regulated financial services company stores its internal engineering standards, architecture decision records, and onboarding guides across a dozen private repositories. They want engineers to ask Copilot Chat natural-language questions like 'What is our approved logging library?' and get answers sourced directly from these internal documents. Which plan and feature combination BEST meets this requirement?

A) Copilot Business with content exclusions configured on the documentation repos
B) Copilot Individual with the Copilot Extensions marketplace enabled
C) Copilot Enterprise with a custom knowledge base built from the documentation repositories
D) Copilot Business with a fine-tuned model trained on the company's codebase

---

**Q2.** A developer wants to type a natural-language request in their terminal, such as 'undo the last two git commits but keep the changes staged,' and receive a suggested shell command with an explanation, without leaving the command line.

A) GitHub Copilot in the CLI
B) GitHub Copilot code review
C) GitHub Copilot Chat in the IDE side panel
D) GitHub Copilot Extensions marketplace

---

**Q3.** An organization on Copilot Business wants to ensure Copilot never surfaces code completions that closely match public code longer than 150 characters, across every developer in the org, without relying on individual editor settings.

A) Enable the 'Suggestions matching public code' blocking policy in the organization's Copilot settings
B) Ask each developer to disable public code suggestions in their personal VS Code settings
C) Add every public repository URL to the organization's content exclusion list
D) Downgrade affected seats to Copilot Individual, which blocks public code matches by default

---

**Q4.** An organization already using Copilot Business is acquired and now belongs to a GitHub Enterprise account that manages several separate organizations. Which capability becomes available only after upgrading to Copilot Enterprise that was not possible under Business?

A) Assigning Copilot seats to individual users within a single organization
B) Applying and enforcing Copilot policies centrally across multiple organizations from the enterprise account
C) Viewing basic Copilot usage metrics for the organization
D) Allowing developers to use Copilot Chat inside their IDE

---

**Q5.** A team wants pull requests to automatically receive AI-generated review comments highlighting potential bugs or style issues on the changed lines, without a human reviewer manually invoking Copilot Chat.

A) GitHub Copilot Extensions
B) GitHub Copilot code review
C) GitHub Copilot in the CLI
D) Inline chat in the IDE

---

**Q6.** A development team uses a third-party project management tool and wants to ask Copilot Chat in their IDE questions like 'summarize the open tickets assigned to me' by pulling live data from that external tool, rather than from GitHub itself.

A) A GitHub Copilot Extension built for that third-party project management tool
B) Content exclusions configured for the project management tool's repository
C) The default Copilot Chat model with no additional configuration
D) A custom knowledge base pointing to the project management tool's export files

---

**Q7.** A financial services company wants Copilot Chat on GitHub.com to answer developer questions using only their curated internal documentation and API specs, without searching across every repository in the enterprise. Which Copilot feature and plan combination BEST meets this need?

A) Copilot Enterprise using Copilot knowledge bases
B) Copilot Business with default Copilot Chat behavior
C) Copilot Individual with public code filtering disabled
D) Copilot Extensions built as GitHub Apps

---

**Q8.** A development team wants to invoke a third-party monitoring tool's live data directly inside Copilot Chat by typing "@monitoring-tool" in the chat window. Which Copilot capability enables this integration?

A) Copilot knowledge bases
B) Copilot in the CLI
C) Copilot code review
D) Copilot Extensions

---

**Q9.** An enterprise admin needs to prevent Copilot from suggesting code that closely matches public code across every organization that belongs to the enterprise account. Where should this policy be configured?

A) Enterprise-level Copilot policy settings applied to all member organizations
B) Each individual user's Copilot settings in their IDE
C) A .copilotignore file placed in each repository
D) The organization's branch protection rules

---

**Q10.** A team lead wants pull requests to automatically include an AI-generated summary of the code changes to speed up code review. Which plan is required to enable this feature?

A) Copilot Individual (Pro)
B) Copilot Business
C) Copilot Free
D) Copilot Enterprise

---

**Q11.** An organization owner using Copilot Business notices that several assigned seats have had no completions or chat activity for 90 days. What should they do to avoid unnecessary billing, per Copilot's seat management capabilities?

A) Enable automatic seat management so inactive seats are automatically unassigned
B) Manually delete each inactive user's GitHub account
C) Downgrade the entire organization to Copilot Individual
D) Wait for GitHub to automatically cancel the subscription after one year

---

**Q12.** A developer wants to translate a natural-language description into a shell command directly from their terminal, without switching to an IDE. Which Copilot feature should they use?

A) Copilot inline chat in VS Code
B) Copilot code review in pull requests
C) Copilot in the CLI
D) Copilot knowledge bases

---

**Q13.** A large enterprise wants developers to ask Copilot Chat questions on GitHub.com and get answers grounded in the content of several internal documentation repositories (READMEs, wikis, architecture docs) rather than just general coding knowledge. Which capability, and under which plan, satisfies this requirement?

A) Copilot Business, using the default Copilot Chat model with no additional configuration
B) Copilot Individual, by pinning the repositories as context in the IDE chat panel
C) Copilot Enterprise, by creating a knowledge base that indexes the specified repositories for Copilot Chat
D) Copilot Business, by enabling the 'suggestions matching public code' policy for those repositories

---

**Q14.** An organization administrator manages GitHub Copilot Business for their organization. They want to prevent Copilot from generating code suggestions that match publicly available code found on GitHub, applying this rule to all seats at once. Where should the administrator make this change?

A) In each developer's personal GitHub account settings under Copilot preferences
B) In the organization's Copilot policy settings, by disabling the 'suggestions matching public code' setting
C) In the repository's branch protection rules under required status checks
D) In the Copilot Chat inline chat settings within Visual Studio Code

---

**Q15.** A financial services company using GitHub Copilot Business wants to minimize legal risk from suggestions that closely match existing public code on GitHub. Which action should the organization take?

A) Ask developers to manually search GitHub before accepting any suggestion
B) Disable Copilot Chat but keep code completions enabled
C) Enable the policy that blocks suggestions matching public code in the Copilot Business admin settings
D) Switch all organization repositories to private visibility

---

**Q16.** Which GitHub Copilot capability inspects other files you currently have open in your editor to build additional context for the current suggestion?

A) Custom instructions files
B) Fine-tuning on your organization's codebase
C) Neighboring tabs
D) The content exclusion policy

---

**Q17.** An administrator enables the policy in GitHub Copilot Business that blocks suggestions matching public code. What is the effect on suggestions shown to developers?

A) Suggestions detected as matching public code above a similarity threshold are filtered out before being shown
B) Only suggestions produced by Copilot Chat are checked; inline code completions are unaffected
C) All code completions across the organization are disabled entirely
D) Only suggestions written in Python are checked for matches

---

**Q18.** What is the primary purpose of the proxy layer that GitHub Copilot requests pass through before a suggestion is returned to the editor?

A) To compile the generated code into an executable binary for testing
B) To apply content filtering, such as blocking offensive output and detecting matches to public code, before returning a suggestion
C) To permanently store the developer's entire repository for future model training
D) To fine-tune the underlying language model in real time using the developer's current code

---

**Q19.** A GitHub Copilot Enterprise customer wants developers to ask Copilot Chat questions and receive answers grounded in the organization's internal repositories and documentation, not only public knowledge. Which feature enables this?

A) The public code matching filter
B) Knowledge bases with repository indexing available in Copilot Enterprise
C) Neighboring tabs context gathering
D) Copilot Individual's saved chat history

---

**Q20.** A developer using GitHub Copilot Individual is concerned that code snippets sent as prompts might be used to train future Copilot models. What setting should they check?

A) The organization's SSO configuration
B) Whether Dependabot alerts are enabled on the repository
C) Whether they have opted in or out of allowing GitHub to use their code snippets for product improvements
D) The repository's branch protection rules

---

**Q21.** An organization uses GitHub Copilot Business. A developer asks why a suggestion in their private repository was blocked. An administrator investigates and finds the suggestion matched a public code snippet longer than 150 characters. Which feature caused this suggestion to be filtered?

A) The proxy server's TLS inspection module
B) The duplication detection filter for matching public code
C) The content exclusion configuration for the repository
D) The vulnerability prevention filter

---

**Q22.** A financial-services company on GitHub Copilot Business wants to prevent Copilot from ever generating suggestions using code stored in a proprietary internal /crypto-keys/ directory, across every repository in the org. Which approach correctly achieves this?

A) Ask each developer to manually disable Copilot inline suggestions while editing files in that folder
B) Rename the folder so Copilot's duplication-detection filter automatically ignores it
C) Configure a content exclusion rule at the organization level in Copilot settings using a path pattern that matches /crypto-keys/
D) Enable 'public code filtering' in each developer's personal Copilot settings

---

**Q23.** Which GitHub Copilot capability specifically blocks a code suggestion from being shown when it matches a contiguous block of 150 characters or more from publicly available code, reducing IP risk?

A) Content exclusions
B) The duplication detection filter
C) Copilot Chat context transparency
D) Organization-level audit logging

---

**Q24.** A developer on GitHub Copilot Individual (Pro) wants their code snippets excluded from being used by GitHub to improve Copilot's suggestion models. What must they do?

A) Nothing — Copilot Individual never uses any user data for model improvement by default
B) Enable the organization-level content exclusion policy for their personal account
C) Adjust their personal Copilot telemetry/data-sharing setting in GitHub account settings to opt out of allowing code snippets to be used for product improvements
D) Ask a GitHub Enterprise administrator to disable telemetry on their behalf, since individual users cannot control this setting

---

**Q25.** A company is comparing GitHub Copilot Business and GitHub Copilot Enterprise for a regulated industry deployment. Which statement about data retention and telemetry differences is accurate?

A) Both plans always store all prompts and suggestions indefinitely for compliance auditing by default
B) Both plans, by default, do not retain a customer's code prompts or suggestions for use in training GitHub's underlying models, with policy administration controlled centrally by the organization/enterprise admin
C) Only Copilot Enterprise disables telemetry collection; Copilot Business always sends full code context to model training pipelines
D) Copilot Business retains all telemetry indefinitely, while Copilot Enterprise deletes it immediately with no retention

---

**Q26.** An organization has configured a content exclusion rule at the organization level to block Copilot from using files matching '**/secrets/**' across all repos. A repository administrator wants to override this and allow Copilot access to a specific secrets folder in only their own repository. What is the correct outcome?

A) The repository-level configuration can override the organization-level exclusion for that specific repository, since repo settings always take precedence
B) The developer can bypass this by disabling Copilot entirely for their IDE, which removes all exclusion enforcement
C) Content exclusions only affect Copilot Chat, so inline code completion in that folder is unaffected regardless of the org policy
D) This is not possible — organization-level content exclusion policies apply org-wide and cannot be overridden or narrowed by repository-level settings

---

**Q27.** A startup's legal team asks whether GitHub provides any contractual protection against third-party intellectual property infringement claims arising specifically from code suggestions generated by Copilot. Which statement is correct?

A) GitHub offers an IP indemnification commitment for eligible Copilot Business and Enterprise customers, provided the customer has enabled the duplication detection (public code) filter and is using the product as intended
B) No GitHub Copilot plan offers any form of IP indemnification; customers bear full legal risk in all cases
C) IP indemnification is offered only to Copilot Individual (Pro) subscribers, not to Business or Enterprise customers
D) IP indemnification applies automatically to all Copilot plans regardless of configuration, with no conditions attached

---

**Q28.** An organization on GitHub Copilot Business wants to prevent Copilot from using code in a specific internal repository as context for suggestions, without disabling Copilot for the rest of the organization. Which feature should they configure?

A) Enable the duplication-detection filter for that repository
B) Revoke the repository's access token from the Copilot application
C) Add the repository to the organization's content exclusion policy in Copilot settings
D) Set the repository visibility to private

---

**Q29.** A company wants to ensure that prompts and suggestions from its developers using GitHub Copilot Business are never retained or used to train GitHub's underlying models. Which statement accurately reflects GitHub's data handling commitment for Copilot Business and Enterprise?

A) Prompts are anonymized but still used to train the model after 30 days
B) Data is retained indefinitely for compliance auditing purposes
C) Only Enterprise plans exclude prompt data from training; Business plans still contribute data
D) Prompts and suggestions are not retained beyond what's needed for abuse detection and are not used to train the underlying models

---

**Q30.** A developer inherits a large, undocumented Python module and needs to quickly understand what a complex function does before modifying it. Which approach BEST uses GitHub Copilot for this task?

A) Open the function in Copilot Chat and use the /explain slash command to get a natural-language walkthrough of the logic
B) Delete the function and ask Copilot to regenerate it from scratch based on the file name
C) Use Copilot's inline code completion to guess what the next line should be without reading the function
D) Ask a teammate to rewrite the function since Copilot cannot analyze existing code

---

**Q31.** A team wants to convert a set of utility functions from JavaScript to Python while preserving behavior. Which Copilot workflow is MOST appropriate?

A) Manually rewrite each function without Copilot since it cannot translate between languages
B) Select the JavaScript code in the editor and ask Copilot Chat to translate it to Python, then review and test the output
C) Ask Copilot to delete the JavaScript files and generate unrelated Python boilerplate
D) Rely solely on Copilot's autocomplete while typing Python from memory of the JavaScript logic

---

**Q32.** Which GitHub Copilot capability is specifically designed to generate unit test cases for an existing function based on its current implementation?

A) Copilot code completion triggered only on comment lines
B) Copilot Chat's /tests slash command
C) GitHub Copilot for CLI's suggest command
D) Copilot's content exclusion configuration in the repository settings

---

**Q33.** A developer wants Copilot to help draft a command-line git operation but is unsure of the exact flags to use. Which tool is BEST suited for this task?

A) Copilot's PR summary generation feature in the pull request UI
B) Copilot code completion inside a .py source file
C) Copilot Chat's /doc slash command
D) GitHub Copilot for CLI, using 'gh copilot suggest' to get a suggested command with an explanation

---

**Q34.** A company is evaluating where GitHub Copilot assistance is and is not appropriate. Which scenario represents an INAPPROPRIATE reliance on Copilot without human review?

A) Directly deploying Copilot-generated authentication and authorization logic to production without any security review
B) Using Copilot-generated code suggestions as a starting point that a developer then reviews and tests before committing
C) Using Copilot to draft a first pass at a commit message, then editing it for accuracy
D) Asking Copilot to explain an unfamiliar regular expression before making changes to it

---

**Q35.** A developer is refactoring a large function to reduce cyclomatic complexity while preserving behavior. What is the RECOMMENDED way to use Copilot Chat for this task?

A) Ask Copilot to rewrite the entire codebase at once to save time
B) Avoid running any tests afterward since Copilot's refactored code is guaranteed correct
C) Select the function and ask Copilot Chat to refactor it, then run the existing test suite to confirm behavior is unchanged
D) Delete the function and let Copilot infer a new one from the surrounding file names

---

**Q36.** A developer using Copilot Chat in VS Code wants an answer that considers code across multiple files in the current repository, not just the file that is open in the editor. Which approach BEST achieves this?

A) Manually open every file in the repository before asking the question
B) Use the /fix slash command instead of a plain question
C) Increase the temperature setting in Copilot Chat settings
D) Type the question in Copilot Chat prefixed with the @workspace participant

---

**Q37.** A developer has a function selected in the editor and wants Copilot Chat to generate unit tests specifically for that function with minimal manual prompt writing. What should they do?

A) Ask Copilot Chat 'What is unit testing?' with no code selected
B) Open a new blank file and ask Copilot to 'write some tests'
C) Use the /doc slash command on the function
D) Select the function and run the /tests slash command in Copilot Chat

---

**Q38.** A developer wants better inline code suggestions from Copilot for a custom data validation pattern used only in their company's codebase. They add two examples of input data and the corresponding correctly validated output directly above the cursor before writing the new function signature. Which prompt engineering technique is this?

A) Zero-shot prompting
B) Chain-of-thought prompting
C) Few-shot prompting
D) Context exclusion

---

**Q39.** A developer keeps 15 unrelated files open in editor tabs while working on a single function, and notices Copilot's inline suggestions are less accurate than expected. What is the MOST likely explanation and BEST fix based on how Copilot uses context?

A) Copilot has a bug and needs to be reinstalled
B) Open, unrelated tabs can dilute the context Copilot uses; closing irrelevant files and keeping only relevant ones open improves suggestion quality
C) Copilot ignores open tabs entirely, so the number of open files has no effect
D) Suggestions degrade only when using Copilot Business, not Copilot Individual

---

**Q40.** A developer needs GitHub Copilot to generate unit tests for a function that must handle null inputs, empty arrays, and boundary values correctly. Which approach BEST leverages Copilot to produce useful, relevant tests?

A) Ask Copilot to generate a single test covering only the happy path input
B) Write a comment or prompt describing the function's edge cases (null, empty, boundary conditions), let Copilot suggest tests based on that context, then review and add any missing cases
C) Invoke Copilot's /tests command with no additional context about which edge cases matter
D) Manually write all tests without using Copilot, since AI-generated tests can never be trusted

---

**Q41.** A team uses GitHub Copilot in VS Code to generate unit tests for a service class. After running a code coverage report, several branches remain untested even though Copilot generated tests for the class. What should the developer do next?

A) Ask Copilot Chat to generate additional tests specifically targeting the uncovered branches (e.g., by referencing the coverage report or the untested lines), then manually verify the new tests assert correct behavior
B) Assume the Copilot-generated tests are complete because they were AI-generated, and skip further review
C) Delete the coverage report, since Copilot-generated tests cannot be evaluated for coverage
D) Switch to a different testing framework, since Copilot does not support improving coverage in the current one

---

**Q42.** A developer wants to generate a complete new test file for an existing, currently untested class directly within the IDE. Which GitHub Copilot capability is BEST suited for this task?

A) Copilot's inline code completion suggestions alone, triggered by typing a test function signature
B) GitHub Copilot in the CLI using 'gh copilot suggest'
C) GitHub Copilot for Pull Requests summary feature
D) The Copilot Chat 'Generate Tests' feature (/tests slash command) within the editor

---

**Q43.** When GitHub Copilot generates unit tests for a function, what remains the developer's most important responsibility?

A) Nothing — Copilot-generated tests are guaranteed to be correct and complete for any function
B) Rewriting every Copilot suggestion from scratch, since Copilot cannot produce valid test syntax
C) Disabling Copilot for test generation entirely, since using AI to write tests violates GitHub's responsible AI guidance
D) Reviewing and validating that the generated tests accurately assert expected behavior and meaningfully cover edge cases, since Copilot may produce plausible-looking but incorrect or incomplete tests

---

**Q44.** A financial services company enables GitHub Copilot Business for its engineering team. Legal wants to reduce the risk of merging code that matches public repositories under restrictive licenses without attribution. Which Copilot feature should the admin enable to address this requirement?

A) Content exclusions for the affected repositories
B) Copilot Chat's explain-code command before every commit
C) Disabling Copilot for all files with a .py or .js extension
D) The duplicate detection filter (code referencing) to block or flag suggestions matching public code

---

**Q45.** During a code review, a senior engineer finds that a Copilot-generated function introduced a SQL injection vulnerability, and it was merged into production. Who is accountable for the vulnerability reaching production?

A) The developer and reviewers who accepted and approved the code without validating it
B) GitHub, because Copilot generated the insecure code
C) No one, since AI-generated code is not covered by standard code review policies
D) The organization's Copilot Business administrator who enabled the license for the team

---

**Q46.** A developer asks GitHub Copilot Chat to generate a database connection function, and the suggestion includes a hardcoded database password string. What is the correct responsible-use action?

A) Accept the suggestion since Copilot only trains on secure coding patterns
B) Report the suggestion to GitHub as a bug and wait for a fix before continuing work
C) Enable the duplicate detection filter so the credential is automatically redacted before insertion
D) Reject or edit the suggestion to remove the hardcoded credential and use a secure secrets management approach instead

---

