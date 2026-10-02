## Chapter 4: Seat Management, Org Policies, and Plan Selection Scenarios — Practice Questions

**Q1.** An Enterprise account contains three Business organizations. The enterprise admin wants each organization owner to decide independently whether to allow Copilot suggestions matching public code, with no enterprise-wide override. Which enterprise policy setting achieves this?

A) Set the policy to Enabled
B) Set the policy to Disabled
C) Remove the policy from the enterprise Copilot settings page
D) Set the policy to No policy

<details>
<summary>Answer</summary>

**Correct: D**

'No policy' at the enterprise level delegates the decision to each organization owner, who can then configure the toggle independently in their org's Copilot policy settings.

**Why the others are wrong:**
- Enabled forces the policy on for all orgs in the enterprise and locks the org-level toggle.
- Disabled forces the policy off for all orgs and locks the org-level toggle.
- There is no 'remove the policy' option — enterprise policies always exist in one of three states: Enabled, Disabled, or No policy.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A developer has been assigned a Copilot Business seat but has not sent a single suggestion request in 95 days. The org admin has enabled automatic seat management. What happens?

A) The seat is automatically reassigned to another user
B) The seat is flagged and automatically removed after 90 days of inactivity
C) Nothing happens unless the admin manually reviews usage
D) The user's GitHub account is suspended

<details>
<summary>Answer</summary>

**Correct: B**

When automatic seat management is enabled, GitHub identifies seats with no Copilot activity for 90 days and automatically removes them to stop billing for unused seats.

**Why the others are wrong:**
- Seats are removed, not transferred — there is no automatic reassignment feature.
- This describes the behavior only when automatic management is OFF; the question specifies it is enabled.
- Copilot seat inactivity has no effect on the user's underlying GitHub account status.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company runs GitHub Enterprise Cloud with multiple organizations and needs centralized audit log streaming for all Copilot seat assignment and policy-change events across every org, plus Copilot Chat answers grounded in internal engineering documentation. Which plan meets both requirements?

A) GitHub Copilot Individual (Pro)
B) GitHub Copilot Enterprise
C) GitHub Copilot Business
D) GitHub Copilot Pro+

<details>
<summary>Answer</summary>

**Correct: B**

Copilot Enterprise adds enterprise-wide audit log streaming and knowledge-base-grounded Copilot Chat (answers sourced from internal docs), neither of which exist in Business or the individual tiers.

**Why the others are wrong:**
- Individual plans have no org/enterprise audit log or policy management at all.
- Business supports org-level audit logs and basic Chat but not enterprise-wide knowledge bases.
- Pro+ is an individual consumer tier with higher premium request allowances, not an org/enterprise product.

</details>

---

**Q4.** An org admin wants to prevent Copilot from ever suggesting code that matches public repositories, organization-wide, with no exceptions per team. Which action correctly configures this?

A) Set 'Suggestions matching public code' to Block in the org's Copilot policy settings
B) Ask each developer to disable telemetry in their IDE settings
C) Remove Copilot seats from all developers
D) Enable Copilot Chat restrictions in the enterprise audit log

<details>
<summary>Answer</summary>

**Correct: A**

The 'Suggestions matching public code' toggle is an org-level (or enterprise-inherited) policy that blocks or allows suggestions duplicating public code; setting it to Block applies org-wide.

**Why the others are wrong:**
- IDE telemetry settings have no effect on the public-code-matching filter, which is server-side.
- Removing seats eliminates Copilot entirely rather than configuring the specific filtering behavior requested.
- Audit logs record events but do not enforce or configure any policy.

</details>

---

**Q5.** A GitHub Enterprise Managed Users (EMU) organization uses SCIM provisioning from its IdP. A developer is removed from the 'Engineering' IdP group that grants Copilot access. What happens to their Copilot seat?

A) The seat is automatically deprovisioned by SCIM when group membership changes
B) The seat remains assigned until an admin manually removes it
C) The developer keeps the seat but loses SSO access
D) Nothing changes because Copilot seats are not tied to SCIM groups

<details>
<summary>Answer</summary>

**Correct: A**

In an EMU environment, SCIM provisioning synchronizes IdP group membership with GitHub team/seat assignments, so removing the user from the mapped group automatically revokes their Copilot seat.

**Why the others are wrong:**
- Manual removal is unnecessary — that's the whole point of automated SCIM provisioning.
- Losing SSO access alone doesn't describe the actual seat deprovisioning outcome tied to group sync.
- Copilot seat assignment can be directly driven by SCIM-synced team membership in EMU orgs.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q6.** Which statement correctly distinguishes Copilot Business from Copilot Enterprise regarding Copilot Chat?

A) Both include Copilot Chat in the IDE, but only Enterprise offers Copilot Chat on github.com grounded with organizational knowledge bases
B) Only Enterprise includes any form of Copilot Chat; Business has no chat feature
C) Business offers unlimited chat requests while Enterprise limits them
D) Enterprise Copilot Chat only works with GitHub Mobile, not IDEs

<details>
<summary>Answer</summary>

**Correct: A**

Both Business and Enterprise provide IDE-based Copilot Chat, but Enterprise adds Copilot Chat on github.com with the ability to ground answers using organization-defined knowledge bases.

**Why the others are wrong:**
- Business does include IDE Copilot Chat, so 'no chat feature' is false.
- Neither tier is described by GitHub as having a hard chat request quota difference framed this way.
- Enterprise Chat works across IDE and github.com, not exclusively on mobile.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** A 40-person startup wants Copilot for all developers, centralized billing on the company's GitHub org, and the ability to block/allow public code matching — but does not need enterprise-wide policy enforcement across multiple orgs or audit log streaming. Which plan is the BEST fit?

A) Copilot Individual (Pro) purchased separately by each developer
B) Copilot Enterprise
C) Copilot Pro+
D) Copilot Business

<details>
<summary>Answer</summary>

**Correct: D**

Copilot Business provides centralized org billing, seat management, and org-level policy toggles including public code matching — exactly matching the stated requirements without paying for Enterprise-only features.

**Why the others are wrong:**
- Individual plans require each developer to pay personally with no centralized billing or org policy control.
- Enterprise is unnecessary since the company explicitly doesn't need multi-org policy enforcement or audit streaming, and it costs more per seat.
- Pro+ is an individual consumer tier, not an org-billed product.

</details>

---

**Q8.** An enterprise administrator sets the 'Copilot in the CLI' policy to Disabled at the enterprise level. An organization owner within that enterprise then tries to enable it in their org's Copilot policy settings. What happens?

A) The org-level toggle overrides the enterprise setting since orgs have final authority
B) The change applies only to new seats assigned after the change
C) GitHub sends a conflict warning but allows the org owner to proceed
D) The setting is grayed out/locked and cannot be changed at the org level

<details>
<summary>Answer</summary>

**Correct: D**

When an enterprise policy is explicitly set to Enabled or Disabled, it locks that setting for every organization in the enterprise — org owners see the toggle but cannot modify it.

**Why the others are wrong:**
- Org-level settings never override an explicit Enabled/Disabled enterprise policy — this is the exact inheritance rule the exam tests.
- The lock applies uniformly regardless of when seats were assigned.
- GitHub does not allow overriding a locked enterprise policy at all, with or without a warning.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

