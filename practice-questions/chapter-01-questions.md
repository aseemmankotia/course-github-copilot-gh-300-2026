## Chapter 1: Copilot Plans and Features: Individual, Business, and Enterprise Tiers — Practice Questions

**Q1.** A 3,000-employee company has one GitHub organization. Leadership wants central control to assign/revoke Copilot seats, enforce a policy blocking suggestions matching public code, and see Copilot usage in the org's audit log. They do NOT need custom knowledge bases or cross-org enterprise policies. Which plan BEST meets these requirements?

A) Copilot Pro+ purchased individually by each employee
B) Copilot Enterprise
C) Copilot Business
D) Copilot Free with org-wide license keys

<details>
<summary>Answer</summary>

**Correct: C**

Copilot Business provides org-level seat management, org policy controls (including public code matching), and audit log entries for Copilot events — exactly what's described, without paying for Enterprise-only features they don't need.

**Why the others are wrong:**
- Copilot Pro+ is billed to individual personal accounts, not centrally managed by an org, and offers no org-level policy or seat control.
- Copilot Enterprise includes everything needed but also adds knowledge bases and enterprise-account (multi-org) policy scope, which the scenario explicitly says isn't required — it's a more expensive superset.
- Copilot Free has no seat management, no org policy controls, and no audit log integration; it's not licensable at org scale.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An enterprise account manages five separate GitHub organizations. It needs to enforce a single Copilot policy across all five orgs simultaneously and give Copilot Chat access to curated internal documentation via knowledge bases. Which plan is required?

A) Copilot Business on each of the five organizations
B) Copilot Pro+ for all developers
C) Copilot Enterprise
D) Copilot Business with enterprise-owned billing

<details>
<summary>Answer</summary>

**Correct: C**

Only Copilot Enterprise supports enterprise-account-level policy controls that apply across multiple organizations, and only Enterprise supports knowledge bases for Copilot Chat.

**Why the others are wrong:**
- Copilot Business policies are configured per organization; there's no single enterprise-wide policy control, and Business lacks knowledge bases.
- Copilot Pro+ is an individual plan with no org or enterprise policy management, and no knowledge base support.
- Business seats can be centrally billed under an enterprise account, but the plan's feature set still lacks cross-org policy enforcement and knowledge bases — that requires upgrading to Enterprise.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A solo developer with a personal GitHub account wants unlimited code completions, in-editor Chat, and CLI support, billed directly to their personal account rather than through an organization. Which plan fits?

A) Copilot Free
B) Copilot Business
C) Copilot Pro
D) Copilot Enterprise

<details>
<summary>Answer</summary>

**Correct: C**

Copilot Pro is the individual paid tier: unlimited completions, Chat, and CLI, billed to the developer's personal GitHub account — no organization involvement required.

**Why the others are wrong:**
- Copilot Free caps completions at 2,000/month and chat at 50 messages/month — not unlimited.
- Copilot Business requires an organization to purchase and assign seats; it isn't billed to an individual's personal account.
- Copilot Enterprise is also org/enterprise-billed and includes far more than a solo developer needs, at a higher seat cost.

</details>

---

**Q4.** Which Copilot feature is available EXCLUSIVELY in Copilot Enterprise, not in Business or Pro?

A) Code completions in the IDE
B) Copilot CLI
C) Knowledge bases for Copilot Chat
D) In-editor Chat

<details>
<summary>Answer</summary>

**Correct: C**

Knowledge bases, which let Copilot Chat reference curated internal documentation, are an Enterprise-only capability.

**Why the others are wrong:**
- Completions are available across Free (limited), Pro, Pro+, Business, and Enterprise.
- Copilot CLI is available in the paid individual and organization tiers, not restricted to Enterprise.
- In-editor Chat is available starting from Copilot Free (limited) through all higher tiers.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** How does Copilot Business/Enterprise billing differ from Copilot Individual (Pro/Pro+) billing?

A) Business/Enterprise use seat-based billing assigned by org/enterprise admins; Individual is billed to a personal account
B) Business/Enterprise charge per repository; Individual charges per organization
C) Individual plans require an enterprise account; Business plans do not
D) There is no difference — all Copilot tiers use identical per-seat billing

<details>
<summary>Answer</summary>

**Correct: A**

Business and Enterprise use a seat-based model where org/enterprise admins assign and revoke seats to members; Individual plans (Pro/Pro+) are self-service and billed directly to the developer's personal account.

**Why the others are wrong:**
- Copilot billing is never per-repository; it's always per-seat/user.
- This reverses reality — Individual plans have nothing to do with enterprise accounts.
- The billing model is fundamentally different: self-billed personal account vs. admin-assigned org seats.

</details>

---

**Q6.** Where do organization owners configure Copilot policies such as disabling suggestions matching public code or restricting Copilot to specific repositories?

A) Personal account Settings > Copilot
B) Repository Settings > Branch protection rules
C) Organization Settings > Copilot > Policies
D) GitHub Marketplace > Copilot listing

<details>
<summary>Answer</summary>

**Correct: C**

Org-level Copilot policy controls (public code matching, feature enablement, repository scoping) live under the organization's Settings > Copilot section, available to Business and Enterprise plans.

**Why the others are wrong:**
- Personal account settings only control an individual's own Copilot Pro/Pro+ preferences, not org policy.
- Branch protection rules govern PR merge requirements, unrelated to Copilot policy configuration.
- The Marketplace listing is for purchasing/installing Copilot, not for ongoing policy management.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A company's Copilot Business seats each include a monthly allowance of premium model requests before additional pay-as-you-go charges apply. What is that included allowance per user?

A) 50 premium requests/month
B) 300 premium requests/month
C) 1000 premium requests/month
D) Unlimited premium requests

<details>
<summary>Answer</summary>

**Correct: B**

Copilot Business includes 300 premium requests per user per month; usage beyond that is billed as pay-as-you-go if enabled by the admin.

**Why the others are wrong:**
- 50 is not a Business allowance figure for premium requests (this number is associated with Copilot Free's monthly chat message cap, a different metric).
- 1000 premium requests/month is the Copilot Enterprise per-user allowance, not Business.
- Premium requests are metered even on paid plans; standard completions are unlimited, but premium model requests are not.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the core distinction between Copilot Individual and Copilot Business/Enterprise from an administrative standpoint?

A) Individual plans are self-managed by the developer; Business/Enterprise are centrally managed by org/enterprise admins with policy and audit controls
B) Individual plans support more programming languages
C) Individual plans require SSO configuration; Business/Enterprise do not
D) Individual plans only work in Visual Studio Code, while Business/Enterprise work in any IDE

<details>
<summary>Answer</summary>

**Correct: A**

The defining administrative difference is governance: Individual is self-service with no central policy or audit capability, while Business/Enterprise give organization/enterprise admins seat management, policy enforcement, and audit log visibility.

**Why the others are wrong:**
- Language support is identical across tiers; it depends on the model, not the plan.
- SSO/enforcement is actually more relevant to Business/Enterprise (via enterprise-managed users), the reverse of this statement.
- IDE compatibility does not vary by plan tier — the same IDE extensions work across Individual, Business, and Enterprise.

</details>

---

