# Answer Key — Practice Test 2

**Q1. Correct: C**

Knowledge bases are a Copilot Enterprise-only feature that let admins curate a set of repositories so Copilot Chat on GitHub.com can answer questions grounded specifically in that documentation.

---

**Q2. Correct: A**

Copilot in the CLI, delivered via the `gh copilot` extension for the GitHub CLI, provides `explain` and `suggest` subcommands specifically to interpret and generate terminal commands without leaving the shell.

---

**Q3. Correct: B**

The public code matching filter is an organization-level Copilot policy (available for Business and Enterprise) that blocks or allows suggestions matching public code above a certain length, and it applies org-wide so legal/compliance requirements are enforced consistently.

---

**Q4. Correct: B**

Copilot Extensions are supported on Copilot Business (not Enterprise-exclusive), but an organization owner must explicitly enable the policy allowing Extensions before members can install and use them from GitHub Marketplace.

---

**Q5. Correct: D**

GitHub Copilot Free provides a limited monthly quota of code completions and chat interactions for any personal GitHub.com account, whereas Copilot Individual (Pro), a paid subscription, removes that cap.

---

**Q6. Correct: B**

Copilot feature policies like 'Copilot in the CLI' are organization-wide toggles that apply to every user with an assigned Copilot seat; there is no per-team scoping mechanism, so the admin must accept the policy applies uniformly or manage access at the seat-assignment level instead.

---

**Q7. Correct: C**

Copilot knowledge bases (a Copilot Enterprise feature) let admins index a curated set of repositories so Copilot Chat on GitHub.com can answer questions grounded in that content automatically.

---

**Q8. Correct: A**

'Suggestions matching public code' is an actual org-level Copilot policy (available on Business/Enterprise) that can be set to Block or Allow for all seats in the organization, enforcing the behavior org-wide.

---

**Q9. Correct: C**

Copilot Extensions let third-party services (like Jira) be surfaced and actioned inside Copilot Chat via @-mentions, extending Copilot's functionality to external tools and APIs.

---

**Q10. Correct: C**

GitHub Copilot in the CLI, accessed as a gh extension, provides 'explain' for breaking down existing commands and 'suggest' for generating shell/git commands directly in the terminal.

---

**Q11. Correct: D**

Copilot Pro+ is the top individual subscription tier, offering the largest monthly premium-request allowance and access to the broadest set of premium models for an individual, non-organization user.

---

**Q12. Correct: B**

Copilot Enterprise builds on top of Copilot Business, adding organization-specific capabilities such as knowledge bases and expanded Copilot Chat integration throughout GitHub.com (pull requests, code search, and more).

---

**Q13. Correct: D**

Content exclusions let Business/Enterprise admins list specific repositories or file paths that Copilot must never use as context for completions or Chat, while leaving normal repository access via GitHub untouched.

---

**Q14. Correct: C**

Copilot Extensions are GitHub Apps that integrate external tools and services into Copilot Chat, exposing custom skills and slash commands with authentication managed through the GitHub App; this is the intended surface for calling an internal service from Chat.

---

**Q15. Correct: A**

GitHub explicitly states that Copilot Business and Enterprise plans do not use customers' code (prompts or suggestions) to train the underlying models, which is a distinct guarantee from the default data-use terms on individual plans.

---

**Q16. Correct: D**

Copilot constructs a prompt using surrounding code in the active file along with context from neighboring open tabs/related files, giving the model localized but richer context without needing the whole repository.

---

**Q17. Correct: D**

When set to Block, Copilot's service-side filtering compares candidate suggestions against public code and suppresses matches at or above roughly 150 characters before they ever reach the editor.

---

**Q18. Correct: C**

Copilot Enterprise knowledge bases build a semantic index over selected repositories/documentation, allowing Copilot Chat to pull relevant context from across the indexed sources rather than being limited to the currently open file.

---

**Q19. Correct: A**

GitHub has expanded Copilot beyond a single OpenAI Codex model, offering model choice (including models from providers like Anthropic and Google in addition to OpenAI) for Copilot Chat in supported plans/IDEs, while inline completions use a default optimized model unless otherwise configured.

---

**Q20. Correct: A**

Content exclusion rules are enforced as an organization-wide policy: matching files are excluded from being used as context and from receiving inline completions, consistently across developers and sessions wherever the policy applies.

---

**Q21. Correct: B**

When the duplicate/public code matching filter is enabled, Copilot checks suggestions against public code and suppresses (blocks) any suggestion matching public code roughly 150 characters or longer, so it is filtered out and never surfaces to the developer.

---

**Q22. Correct: D**

For Copilot Business and Enterprise, GitHub does not retain or use customer prompts/suggestions data to train the underlying models; the request/response data is processed to generate suggestions and then handled according to GitHub's data retention policy, not used for model training.

---

**Q23. Correct: D**

Copilot Enterprise builds a semantic index of the organization's repositories, allowing Copilot Chat to retrieve relevant snippets from across the codebase (not just open files) and inject them as context automatically, without the developer manually pasting code.

---

**Q24. Correct: B**

Content exclusions are additive and security-first: organization-level and repository-level exclusion rules combine, and the most restrictive applicable rule always wins. Repository settings cannot un-exclude files that an organization has excluded.

---

**Q25. Correct: D**

Repository-scoped content exclusions are defined in `.github/copilot.yml`, specifying glob patterns under an exclude/content-exclusion key, which Copilot Business/Enterprise honors when building context.

---

**Q26. Correct: A**

Copilot Business/Enterprise admins can set an org-wide policy for the duplication-detection (public code matching) filter that locks the setting for all members, whereas Copilot Individual only exposes this as a personal, per-user toggle with no centralized enforcement.

---

**Q27. Correct: C**

GitHub's Copilot IP indemnification commitment is extended to Business and Enterprise customers and is conditioned on having the filter that blocks suggestions matching public code turned on, among other required settings.

---

**Q28. Correct: C**

GitHub differentiates data handling by plan: Copilot Individual users can opt in/out of allowing their code snippets to be used for product improvement/training, while Copilot Business and Enterprise contractually guarantee customer prompts and code are not used to train GitHub's models.

---

**Q29. Correct: B**

Content exclusions apply uniformly across Copilot's features, including both code completions and Copilot Chat — an excluded file is not read into context for either, and Chat will indicate it cannot access that file.

---

**Q30. Correct: B**

Content exclusions are scoped per repository/path — the excluded file is fully removed both as a suggestion target and as context, but it has no effect on other repositories or files that aren't covered by an exclusion rule; those continue operating normally.

---

**Q31. Correct: D**

/explain in Copilot Chat is purpose-built for summarizing selected code in natural language, giving the developer the context needed before making a safe edit — this is the core 'explain unfamiliar code' use case tested on the exam.

---

**Q32. Correct: A**

GitHub Copilot integrates directly into the pull request creation flow on GitHub.com, generating a summary of the diff so reviewers get context without any local tooling — matching the exact requirement of 'without leaving the PR page'.

---

**Q33. Correct: A**

Copilot's output quality depends heavily on context in the prompt and open files; adding explicit comments about edge cases and keeping relevant test files open gives the model the signal needed to produce more relevant, thorough tests.

---

**Q34. Correct: C**

/tests is the built-in Copilot Chat slash command that generates unit tests for the selected code block.

---

**Q35. Correct: D**

Copilot Chat with the full source file open as context and an explicit instruction on target language/conventions produces the most coherent translation because it can reason about the whole script's logic and structure at once, followed by mandatory human review and testing.

---

**Q36. Correct: B**

Cryptographic implementations require formal security review and proven, audited algorithms; accepting AI-generated crypto code without expert review risks subtle vulnerabilities that are hard to detect through normal testing — this is a core responsible-AI-use boundary tested on the exam.

---

**Q37. Correct: A**

@workspace is designed to search and reason across the entire indexed codebase (not just open files), making it the correct tool for cross-file usage discovery before a refactor.

---

**Q38. Correct: C**

@github exposes GitHub-specific skills and knowledge (repositories, issues, PRs, and Actions runs) via Copilot Chat on github.com, allowing it to reason about workflow failures using real repository data.

---

**Q39. Correct: B**

The #file: reference syntax explicitly attaches a specific file's contents as context to the chat prompt, scoping the answer to that file.

---

**Q40. Correct: B**

Few-shot prompting provides concrete input/output examples as context, which anchors Copilot's output to the demonstrated pattern, structure, and conventions.

---

**Q41. Correct: A**

Copilot's initial output often reflects only the most common patterns; providing a specific, edge-case-focused prompt directs it toward the missing scenarios, and manual review is still required to validate that the generated assertions are meaningful.

---

**Q42. Correct: D**

Tests that never fail regardless of code changes typically contain weak assertions (e.g., checking that a function 'runs' rather than checking specific output values); GitHub's Copilot guidance stresses that AI-generated tests must always be reviewed and validated by a human before being trusted.

---

**Q43. Correct: A**

The /tests slash command in Copilot Chat is purpose-built to generate unit tests for a selected piece of code within the IDE, using surrounding context to infer the appropriate test framework and structure.

---

**Q44. Correct: C**

Copilot relies heavily on contextual signals — open files, existing test patterns, imports, and naming conventions — to align generated code with the project's established style, so it would likely follow the existing pytest fixtures and parametrization patterns already in the repo.

---

**Q45. Correct: A**

The public code matching filter is designed to detect exact or near-exact matches against public code on GitHub. Suggestions that are semantically similar but not textually matching (e.g., refactored, renamed, or restructured) can slip past the filter, which is a known limitation exam candidates must understand.

---

**Q46. Correct: B**

GitHub's responsible-AI positioning is explicit that Copilot is a pair programmer whose suggestions require human review, testing, and validation before acceptance. Accountability for accepted and shipped code rests with the developer and team who reviewed and merged it, not the tool itself.

---

**Q47. Correct: C**

The public code matching filter is the feature designed to detect and optionally block suggestions that match public code on GitHub, which is the primary built-in mechanism for reducing the risk of reproducing license-restricted snippets without attribution.

---

