## Chapter 10: Responsible AI and Ethical Use of Copilot — Practice Questions

**Q1.** A developer's pull request contains Copilot-suggested code that introduces a production outage. The developer states the bug is 'Copilot's fault' during the incident review. Per GitHub's Responsible AI guidance, who is accountable for the merged code?

A) GitHub, because Copilot generated the suggestion
B) No one, since AI-generated code is not attributable to a human
C) The Copilot model provider that trained the underlying LLM
D) The developer who accepted and merged the suggestion

<details>
<summary>Answer</summary>

**Correct: D**

GitHub's human accountability principle states developers remain fully responsible for any code they accept and commit, regardless of whether Copilot suggested it — the tool assists, it does not own outcomes.

**Why the others are wrong:**
- GitHub provides the tool but does not review, approve, or own code merged into a repository
- Human accountability explicitly means AI suggestions do not remove responsibility from the person who merges them
- Model providers are not accountable for how individual developers use suggestions in production systems

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** During code review, a teammate flags that a Copilot suggestion is nearly identical to a snippet from a public GPL-licensed repository. What is the correct immediate action?

A) Merge it since Copilot suggestions are always safe to use
B) Add a comment crediting Copilot and merge as-is
C) Disable code review for AI-suggested changes going forward
D) Remove or rewrite the matching code and verify licensing before merging

<details>
<summary>Answer</summary>

**Correct: D**

Suggestions matching public code can carry license obligations (e.g., attribution or copyleft terms). The safe practice is to remove/rewrite the match or confirm license compatibility before merge.

**Why the others are wrong:**
- Copilot suggestions are not guaranteed license-safe; matches to public code carry real legal risk
- Crediting Copilot does not satisfy the original license's attribution or copyleft terms
- Disabling review entirely increases risk rather than mitigating it

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A reviewer notices Copilot suggested a database query built via string concatenation of user input. What is the exam-correct response?

A) Accept it since Copilot suggestions are pre-vetted for security
B) Merge it and rely on GitHub Advanced Security to fix it automatically post-merge
C) Reject or modify it to use parameterized queries, applying the same security review as human-written code
D) Ignore it because SQL injection risk does not apply to AI-suggested code

<details>
<summary>Answer</summary>

**Correct: C**

Copilot-suggested patterns require the same security scrutiny as any code — string-concatenated queries are a classic SQL injection risk and must be corrected to parameterized queries before merge.

**Why the others are wrong:**
- Copilot does not guarantee secure code; it can reproduce insecure patterns seen in training data
- Code scanning tools flag issues but do not silently rewrite them; the developer must remediate
- Security risk in code is independent of its origin (human or AI-suggested)

</details>

---

**Q4.** Which GitHub Copilot policy setting reduces the risk of merging code that duplicates licensed public repository content?

A) Content exclusions
B) Suggestions matching public code
C) Copilot Chat access policy
D) IDE Completions toggle

<details>
<summary>Answer</summary>

**Correct: B**

The 'Suggestions matching public code' setting filters out (or flags) Copilot suggestions that closely match public code, directly reducing licensing/attribution risk.

**Why the others are wrong:**
- Content exclusions prevent specific files/paths from being used as Copilot context, unrelated to public code matching
- Copilot Chat access policy controls who can use Chat, not licensing risk in completions
- IDE Completions toggle simply enables/disables inline suggestions entirely

</details>

---

**Q5.** Which tool should a team integrate into their CI pipeline to systematically scan Copilot-suggested code for vulnerabilities before merge?

A) GitHub Advanced Security code scanning (CodeQL)
B) Copilot Chat inline explanations
C) Copilot Workspace
D) Dependabot version updates

<details>
<summary>Answer</summary>

**Correct: A**

CodeQL-based code scanning under GitHub Advanced Security automatically analyzes code — including AI-suggested code — for known vulnerability patterns as part of CI, supporting the security review principle.

**Why the others are wrong:**
- Chat explanations describe code but do not perform automated vulnerability scanning
- Copilot Workspace assists with planning/implementing changes, not security scanning
- Dependabot addresses vulnerable dependencies, not vulnerable patterns within authored code

</details>

---

**Q6.** An Enterprise admin wants to block all Copilot suggestions that closely match public repository code for every organization under the enterprise. Where is this configured?

A) Each developer's personal Copilot settings individually
B) Repository-level branch protection rules
C) Enterprise account > Policies > Copilot > Suggestions matching public code (set to Blocked)
D) The .github/copilot-instructions.md file

<details>
<summary>Answer</summary>

**Correct: C**

Enterprise administrators set Copilot policies centrally at the enterprise level, which can enforce 'Blocked' for public code matching across all managed organizations.

**Why the others are wrong:**
- Personal settings only apply to Individual plans and can be overridden by enterprise policy
- Branch protection rules govern merge requirements, not Copilot suggestion filtering
- The instructions file customizes Copilot behavior/context, not licensing filters

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A developer notices Copilot repeatedly generates code comments and variable names reflecting stereotypical assumptions (e.g., defaulting gendered pronouns in examples). What responsible AI concept does this illustrate?

A) Model hallucination
B) A licensing violation
C) Bias present in AI-generated output reflecting training data patterns
D) A security vulnerability

<details>
<summary>Answer</summary>

**Correct: C**

Copilot is trained on large public datasets and can reproduce societal biases present in that data; developers must review and correct such output as part of responsible use.

**Why the others are wrong:**
- Hallucination refers to factually incorrect or fabricated output, not biased phrasing
- This scenario involves fairness/bias, not code licensing
- This scenario is not a security concern; it's a fairness/bias concern

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** Which principle best describes the requirement that every Copilot suggestion be reviewed by a human before it is committed to a codebase?

A) Transparency
B) Data minimization
C) Model interpretability
D) Human-in-the-loop / human accountability

<details>
<summary>Answer</summary>

**Correct: D**

Human accountability (human-in-the-loop) requires that a person validate and take ownership of AI-suggested code before it becomes part of the product — Copilot assists, humans decide.

**Why the others are wrong:**
- Transparency concerns disclosing that AI was used, not the review requirement itself
- Data minimization relates to limiting data collection/exposure, unrelated here
- Interpretability concerns understanding model reasoning, not the review workflow

</details>

---

