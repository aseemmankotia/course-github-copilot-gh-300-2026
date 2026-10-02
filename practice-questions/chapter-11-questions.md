## Chapter 11: Cross-Domain Review: Scenario-Based Judgment Drills — Practice Questions

**Q1.** A global company wants to enforce a single Copilot policy (blocking public code matching suggestions) across five separate GitHub organizations from one central place. Which plan BEST meets this requirement?

A) GitHub Copilot Business
B) GitHub Copilot Enterprise
C) GitHub Copilot Pro+
D) GitHub Copilot Free

<details>
<summary>Answer</summary>

**Correct: B**

Enterprise account settings let admins enforce Copilot policies centrally across every organization owned by the enterprise.

**Why the others are wrong:**
- Business manages policies per-organization only; it cannot centrally enforce one policy across five separate orgs.
- Pro+ is an individual-tier plan with no organizational policy controls at all.
- Free has no admin policy controls or org-level management features.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer on GitHub Copilot Individual wants to prevent Copilot from ever suggesting code based on a folder of proprietary internal libraries across their organization. What must happen first?

A) The organization must upgrade to Copilot Business or Enterprise, since content exclusion is not available on Individual plans
B) Add the folder to .gitignore so Git ignores it
C) Disable the Copilot telemetry setting in personal preferences
D) Rename the folder so Copilot cannot parse the file extensions

<details>
<summary>Answer</summary>

**Correct: A**

Content exclusion (path-based suggestion blocking) is only available on Business and Enterprise plans, configured at the org level.

**Why the others are wrong:**
- .gitignore controls Git tracking, not Copilot's content exclusion feature — it has no effect on suggestions.
- The telemetry setting controls data usage for product improvement, not path-based content exclusion.
- Renaming files has no bearing on Copilot's suggestion engine or exclusion policy.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** An enterprise's legal team is concerned about Copilot suggesting code that closely matches existing public repositories, creating potential license exposure. Which setting directly addresses this concern?

A) Enable the public code matching (duplication detection) filter at the org or enterprise level
B) Enable content exclusion for all repositories
C) Disable Copilot Chat for all users
D) Enable GitHub Advanced Security code scanning

<details>
<summary>Answer</summary>

**Correct: A**

The public code matching filter blocks suggestions that match public code of 150+ characters, directly reducing license/IP exposure risk.

**Why the others are wrong:**
- Content exclusion hides internal files from Copilot's context — it does not filter suggestions matching public code.
- Disabling Chat removes a conversational feature but does not address code-completion license risk.
- Advanced Security code scanning finds vulnerabilities, not license-matching public code duplication.

</details>

---

**Q4.** A company wants employees to ask Copilot Chat questions on github.com that pull answers from an internally curated knowledge base of engineering documentation. Which plan is required?

A) GitHub Copilot Business
B) GitHub Copilot Enterprise
C) GitHub Copilot Pro
D) GitHub Copilot Free

<details>
<summary>Answer</summary>

**Correct: B**

Knowledge Bases integrated with Copilot Chat on github.com are an Enterprise-only capability.

**Why the others are wrong:**
- Business includes Copilot Chat in the IDE and github.com but not curated Knowledge Bases.
- Pro is an individual consumer plan with no organizational knowledge base support.
- Free provides only limited chat/completions with no enterprise knowledge integration.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** An org admin needs to toggle the 'suggestions matching public code' filter for their entire organization. Where is this configured?

A) Repository Settings > Security > Code scanning
B) Personal Settings > Copilot
C) Organization Settings > Copilot > Policies
D) Enterprise Billing > Usage

<details>
<summary>Answer</summary>

**Correct: C**

Copilot content-related policies, including the public code matching filter, are managed under Organization Settings > Copilot > Policies (or inherited from an Enterprise account).

**Why the others are wrong:**
- Code scanning settings relate to Advanced Security vulnerability detection, not Copilot suggestion filtering.
- Personal Copilot settings only affect that individual's own account, not org-wide policy.
- Billing/usage settings track consumption and cost, not feature policies.

</details>

---

**Q6.** What is the primary risk that GitHub Copilot's public code matching filter is designed to mitigate?

A) Prompt injection attacks against the model
B) Hallucinated API method names
C) Excessive Copilot API token consumption
D) License and intellectual property exposure from code resembling public repositories

<details>
<summary>Answer</summary>

**Correct: D**

The filter blocks completions that duplicate 150+ characters of known public code, protecting against license/IP risk.

**Why the others are wrong:**
- Prompt injection is a security concern unrelated to this specific filter.
- Hallucinated APIs are a model-accuracy issue, not addressed by public code matching.
- Token usage is a cost/performance concern, not what this filter targets.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** During QA, Copilot Autofix generates a suggested remediation for a code scanning security alert. What is the BEST next step before merging the fix?

A) Merge immediately since Autofix suggestions are pre-validated
B) Permanently disable Autofix to avoid future risk
C) Skip review since automated tests will catch any issue
D) Have a human reviewer verify the fix and run existing tests before merging

<details>
<summary>Answer</summary>

**Correct: D**

Responsible AI guidance requires human review of all AI-generated code, including Autofix suggestions, before merge.

**Why the others are wrong:**
- Autofix suggestions are AI-generated and not guaranteed correct or complete; auto-merging violates responsible AI practice.
- Disabling Autofix removes a useful security tool rather than addressing the review gap.
- Automated tests alone may not catch logic, security, or business-context issues introduced by the fix.

</details>

---

**Q8.** A developer wants more relevant Copilot completions when writing a new payment-processing function. Which technique is BEST supported by Copilot's prompt engineering guidance?

A) Write a single-word placeholder and let Copilot infer everything
B) Close all other files to reduce noise in the editor
C) Add descriptive comments stating the intent and keep related files open for context
D) Disable multi-file context so Copilot only sees the current line

<details>
<summary>Answer</summary>

**Correct: C**

Providing descriptive comments and relevant open-file context is the documented best practice for improving Copilot suggestion quality.

**Why the others are wrong:**
- Vague single-word prompts produce vague, lower-quality completions.
- Closing related files removes useful context Copilot uses to generate relevant suggestions.
- Disabling multi-file context reduces the contextual signal Copilot relies on for accuracy.

</details>

---

