## Chapter 6: Privacy Fundamentals and Context Exclusions — Practice Questions

**Q1.** An enterprise organization wants to prevent GitHub Copilot from using files in a 'finance-secrets' repository as context anywhere across the org, without depending on individual repo admins to configure anything. Which approach BEST meets this requirement?

A) Ask each repository admin to add a repository-level content exclusion file
B) Revoke Copilot licenses for any user who can access that repository
C) Enable the duplication-detection filter for the organization
D) Configure an organization-level content exclusion rule targeting the finance-secrets repository

<details>
<summary>Answer</summary>

**Correct: D**

Organization-level content exclusion rules are configured once by org owners and apply org-wide, independent of individual repo admin action.

**Why the others are wrong:**
- Relies on every repo admin acting correctly — not centrally enforced and error-prone
- Removes Copilot access entirely rather than just excluding content, and is overly broad
- The duplication-detection filter controls suggestions matching public code, not private content exclusion

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** A repository admin has configured a repository-level content exclusion for /secrets/**, but the organization's Copilot policy has disabled repository-level exclusion configuration for all repos. What is the result?

A) The repository-level rule overrides the organization policy since it is more specific
B) Both rules are merged and enforced together automatically
C) The repository-level rule is ignored because the org has disabled repo-level configuration
D) Copilot stops functioning entirely in that repository

<details>
<summary>Answer</summary>

**Correct: C**

When an organization disables repository-level exclusion configuration, any repo-level rules are not enforced; only org-level rules apply.

**Why the others are wrong:**
- Repo-level rules never override an org policy that disables them
- There is nothing to merge if repo-level configuration is disabled at the org
- Copilot continues to function normally; it simply won't honor the disabled repo-level rule

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A company wants Copilot to stop offering code completions that closely match publicly available code on GitHub, to reduce licensing risk. Which setting should be enabled?

A) Suggestions matching public code = Block (duplication-detection filter)
B) Content exclusions
C) Telemetry opt-out
D) Repository visibility restriction

<details>
<summary>Answer</summary>

**Correct: A**

The duplication-detection filter, exposed as the 'Suggestions matching public code' setting, blocks suggestions that match public code when set to Block.

**Why the others are wrong:**
- Content exclusions control which files Copilot can use as context, not public-code matching
- Telemetry settings govern data collection/retention, not suggestion filtering
- Repository visibility has no effect on Copilot's suggestion filtering behavior

</details>

---

**Q4.** A team of solo developers uses GitHub Copilot Pro (Individual) with no organization account. They want to configure repository-level content exclusions. What must they do?

A) Upgrade to Copilot Business or Enterprise, since content exclusions are not supported on Individual plans
B) Nothing — content exclusions are available on all Copilot plans
C) Add a .gitignore entry for the sensitive paths
D) Configure exclusions through personal account settings API

<details>
<summary>Answer</summary>

**Correct: A**

Content exclusions are an organization-managed feature available only on Copilot Business and Enterprise plans.

**Why the others are wrong:**
- Individual/Pro plans have no content exclusion capability at all
- .gitignore controls git tracking, not Copilot context usage
- There is no personal-account API for content exclusions — it's an org-governed feature

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** Which GitHub Copilot plans support organization-level content exclusion configuration?

A) Copilot Free and Pro
B) All Copilot plans equally
C) Copilot Business and Enterprise only
D) Copilot Individual only

<details>
<summary>Answer</summary>

**Correct: C**

Content exclusion, at both org and repo level, is exclusive to Copilot Business and Enterprise.

**Why the others are wrong:**
- Free and Pro are individual plans without organizational policy controls
- Not all plans support this feature — it's Business/Enterprise only
- Individual has no organization-level policy layer to configure

</details>

---

**Q6.** How are organization-level content exclusion rules typically defined?

A) A YAML block in the organization's Copilot policy settings specifying repository name and an array of paths
B) A .github/copilot.yml file committed to each individual repository
C) A JSON file stored at the root of the organization's default repo
D) A copilot-exclude.json file committed to the .github special repository

<details>
<summary>Answer</summary>

**Correct: A**

Org-level exclusions are entered as YAML in the organization's Copilot settings UI, specifying repo names and gitignore-style path patterns to exclude.

**Why the others are wrong:**
- There is no per-repo copilot.yml mechanism for org-level rules
- Exclusions are not stored as a JSON file in a repo
- The .github repo special file convention is not used for content exclusions

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q7.** What is GitHub's default data-privacy commitment for Copilot Business and Enterprise regarding private repository code and model training?

A) Private code is used to fine-tune the underlying model unless customers opt out
B) Only public repositories are excluded from training; private repos are included by default
C) Prompts and suggestions from Business/Enterprise customers are not used to train GitHub's models
D) Training data usage depends on a per-repository visibility toggle

<details>
<summary>Answer</summary>

**Correct: C**

GitHub commits contractually that Business/Enterprise customer prompts and code suggestions are not used to train its models — this is not configurable, it's guaranteed by default.

**Why the others are wrong:**
- This is the opposite of GitHub's stated commitment
- Visibility of the repo is irrelevant to this training commitment
- There is no per-repo toggle controlling model training use

</details>

---

**Q8.** A developer wants to confirm, while editing in VS Code, that content exclusion is actively preventing Copilot from using the current file as context. What should they check?

A) Check the Copilot status icon in the editor status bar, which indicates when the file is excluded
B) Run a 'gh copilot exclusions verify' CLI command
C) Inspect network request logs for blocked calls
D) There is no way to verify enforcement; the admin must trust the configuration

<details>
<summary>Answer</summary>

**Correct: A**

The Copilot status bar icon in supported editors changes state and displays a message when the current file matches a content exclusion rule.

**Why the others are wrong:**
- No such CLI command exists for verifying exclusions
- Network log inspection isn't a documented or practical verification method
- Enforcement can be verified directly in the editor UI

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

