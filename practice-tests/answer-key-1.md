# Answer Key — Practice Test 1

**Q1. Correct: C**

Custom knowledge bases that let Copilot Chat ground its answers in specific internal repositories and documents are a Copilot Enterprise-only capability, exactly matching the described requirement.

---

**Q2. Correct: A**

GitHub Copilot in the CLI (installed as a GitHub CLI extension) provides 'gh copilot suggest' and 'gh copilot explain' to turn natural-language requests into shell/git commands with explanations, directly in the terminal.

---

**Q3. Correct: A**

Organization owners on Copilot Business/Enterprise can enforce a policy that blocks suggestions matching public code over a certain length org-wide; this is managed centrally, not per developer.

---

**Q4. Correct: B**

Copilot Enterprise adds enterprise-account-level administration, letting policies and seat management be applied consistently across multiple organizations under one enterprise—something Business, scoped to a single org, cannot do.

---

**Q5. Correct: B**

Copilot code review is the feature purpose-built to analyze pull request diffs and automatically post review comments on the changed lines, either on request or automatically depending on repository configuration.

---

**Q6. Correct: A**

Copilot Extensions are designed to integrate third-party tools and services as agents inside Copilot Chat, allowing developers to query live external data (like ticket status) using natural language.

---

**Q7. Correct: A**

Knowledge bases are a Copilot Enterprise-only feature that let admins curate specific sets of Markdown documentation for Copilot Chat to reference on GitHub.com, scoping answers to that content instead of the entire org.

---

**Q8. Correct: D**

Copilot Extensions are built on GitHub Apps and let third-party or custom tools be invoked from Copilot Chat using an @-mention, bringing external context and actions directly into the chat interface.

---

**Q9. Correct: A**

Enterprise owners can set Copilot policies (including the 'suggestions matching public code' filter) at the enterprise level, which cascades to and enforces the setting across all member organizations.

---

**Q10. Correct: D**

Automatically generated pull request summaries are a Copilot Enterprise feature, layered on top of the Business plan's capabilities and tied to GitHub.com-integrated Copilot experiences.

---

**Q11. Correct: A**

Copilot Business and Enterprise support automatic seat management, which can unassign seats from members who show no Copilot activity for a defined period, reducing wasted spend without manual intervention.

---

**Q12. Correct: C**

Copilot in the CLI (invoked via the gh CLI extension, e.g. 'gh copilot suggest') converts natural-language descriptions into shell commands, git commands, or gh commands directly in the terminal.

---

**Q13. Correct: C**

Knowledge bases are a Copilot Enterprise-only feature on GitHub.com. An admin curates a set of repositories into a knowledge base, and Copilot Chat then uses that indexed content to ground its answers to organization-specific questions.

---

**Q14. Correct: B**

Organization owners/admins with Copilot Business or Enterprise control this behavior centrally through org-level Copilot policies, including the toggle for suggestions matching public code, which applies to all assigned seats.

---

**Q15. Correct: C**

Copilot Business/Enterprise admins can enable a policy that filters out suggestions detected as matching public code, directly addressing the IP/legal risk without disabling the tool entirely.

---

**Q16. Correct: C**

Neighboring tabs is the mechanism by which Copilot scans other open files in the editor to gather relevant context and improve suggestion relevance for the file being edited.

---

**Q17. Correct: A**

When enabled, this policy filters suggestions that are detected as duplicating public code before they reach the developer, rather than disabling Copilot outright.

---

**Q18. Correct: B**

The proxy sits between the client and the model, applying filtering such as toxicity/offensive content blocking and public code match detection before a suggestion is delivered.

---

**Q19. Correct: B**

Copilot Enterprise supports knowledge bases that index an organization's repositories and documentation so Copilot Chat can ground its answers in that internal context.

---

**Q20. Correct: C**

Copilot Individual provides a personal setting controlling whether code snippets and related telemetry can be used by GitHub for product/model improvement, which is the relevant opt-in/opt-out control.

---

**Q21. Correct: B**

Copilot Business/Enterprise includes a filter that checks suggestions against public code and blocks or flags matches of roughly 150 characters or more (configurable to block or show with citation), which is exactly the scenario described.

---

**Q22. Correct: C**

Copilot Business and Enterprise support content exclusions configured at the organization level (or repository level via a config file), using path glob patterns that apply automatically to every developer and repository matched, without relying on manual per-user action.

---

**Q23. Correct: B**

The duplication detection filter (public code matching filter) compares generated suggestions against public code on GitHub and suppresses or flags matches above a defined length threshold, specifically to reduce the risk of surfacing copyrighted public code verbatim.

---

**Q24. Correct: C**

Individual Copilot users can control, in their personal GitHub account settings, whether GitHub is permitted to use their code snippets and telemetry to improve Copilot; this opt-out is a self-service, per-user setting rather than an organizational or admin-only control.

---

**Q25. Correct: B**

For both Copilot Business and Copilot Enterprise, GitHub's stated commitment is that customer prompts and code suggestions are not retained for training GitHub's foundation models, and policy-level controls (such as content exclusions and data-handling policies) are configured centrally by org/enterprise admins rather than per individual developer.

---

**Q26. Correct: D**

Organization-level content exclusion policies are enforced centrally and apply across all repositories in scope; individual repository administrators cannot override or narrow an org-wide exclusion rule, ensuring consistent governance over sensitive content.

---

**Q27. Correct: A**

GitHub has publicly committed to defending and indemnifying eligible Copilot Business and Enterprise customers against certain IP infringement claims arising from suggestions, conditioned on the customer using GitHub's responsible-use safeguards such as the duplication detection filter.

---

**Q28. Correct: C**

Content exclusions let organization admins (Business/Enterprise) specify paths or entire repositories that Copilot must not use as context, via a .github/copilot.yml file or org-level policy, while Copilot remains enabled elsewhere.

---

**Q29. Correct: D**

For Copilot Business and Enterprise, GitHub commits that customer prompts and code snippets are not used to train the foundation models, and retention is limited to short-term operational needs like abuse monitoring.

---

**Q30. Correct: A**

/explain in Copilot Chat is purpose-built to summarize and clarify existing code, including unfamiliar legacy logic, directly in context.

---

**Q31. Correct: B**

Copilot Chat supports code translation between languages when given the source code as context, and generated output should always be reviewed and tested.

---

**Q32. Correct: B**

The /tests slash command in Copilot Chat is purpose-built to generate unit tests for selected code based on its logic and existing patterns.

---

**Q33. Correct: D**

GitHub Copilot for CLI is designed specifically to suggest and explain terminal commands, including git operations, based on a natural-language description.

---

**Q34. Correct: A**

Security-sensitive code like authentication and authorization requires human expert review because Copilot suggestions can contain subtle vulnerabilities or omissions; deploying without review is an inappropriate, high-risk use of AI assistance.

---

**Q35. Correct: C**

Copilot Chat can refactor selected code for clarity or complexity, but the developer must validate behavior preservation by running existing tests afterward.

---

**Q36. Correct: D**

The @workspace chat participant indexes and searches the current workspace/repository so Copilot Chat can pull in relevant context from multiple files when answering, rather than being limited to the active editor tab.

---

**Q37. Correct: D**

The /tests slash command is purpose-built to generate unit tests for the selected code, using the selection as direct context so Copilot produces relevant, targeted test cases.

---

**Q38. Correct: C**

Providing concrete input/output examples in the prompt/context before asking Copilot to complete a similar new case is few-shot prompting — it primes the model with patterns to follow, improving suggestion relevance for codebase-specific conventions.

---

**Q39. Correct: B**

Copilot uses nearby and recently viewed open files as part of its contextual signal for inline suggestions; keeping only relevant files open narrows that context to what's useful, improving suggestion relevance and quality.

---

**Q40. Correct: B**

Copilot's suggestions are heavily influenced by the surrounding context and prompt. Explicitly describing edge cases in a comment or chat prompt gives Copilot the information it needs to generate targeted tests for null, empty, and boundary conditions, and the developer still reviews the output for gaps — the recommended workflow the exam expects.

---

**Q41. Correct: A**

Copilot can iteratively improve test coverage when given specific context, such as which branches or lines are untested. Prompting Copilot Chat with that information yields targeted new tests, but the developer must still manually validate the generated assertions are correct — reflecting Copilot's role as an assistant, not a replacement for developer judgment.

---

**Q42. Correct: D**

Copilot Chat's dedicated test-generation capability (the /tests slash command or 'Generate Tests' action) is purpose-built for producing a complete test file or test suite for a selected class or function, making it the most direct and efficient tool for this scenario.

---

**Q43. Correct: D**

GitHub's Copilot documentation and exam objectives emphasize that AI-generated content, including tests, must always be reviewed and validated by the developer. Copilot can produce tests that compile and look reasonable but assert incorrect behavior or miss important edge cases, so human verification remains essential.

---

**Q44. Correct: D**

GitHub Copilot Business/Enterprise includes a duplicate detection (code referencing) filter that checks suggestions against public code on GitHub and can block or surface matches longer than ~150 characters, along with the matching repository and license, letting teams manage attribution/licensing risk directly.

---

**Q45. Correct: A**

GitHub's responsible-use guidance is explicit that Copilot is a pair programmer, not an accountable party: developers and reviewers remain fully responsible for validating, testing, and securing any suggestion before it is accepted and merged, regardless of its source.

---

**Q46. Correct: D**

Copilot can suggest insecure patterns, including hardcoded secrets, because it predicts plausible code rather than guaranteeing security; responsible use requires the developer to review, reject, or edit such suggestions and apply secure practices like environment variables or a secrets manager.

---

