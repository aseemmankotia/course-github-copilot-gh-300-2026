## Chapter 10: Responsible AI and Ethical Use of Copilot — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Who is accountable when Copilot-suggested code causes a bug after merge? | The human developer who reviewed and merged it — human accountability principle applies regardless of AI assistance. |
| 2 | Copilot setting that filters/blocks suggestions closely matching public repositories | 'Suggestions matching public code' — reduces licensing/attribution risk. Available for Individual, Business, and Enterprise. |
| 3 | Where does an Enterprise admin enforce 'Suggestions matching public code' org-wide? | Enterprise account > Policies > Copilot settings — policy can be locked to apply to all member organizations. |
| 4 | Tool used to scan Copilot-suggested code for security vulnerabilities in CI | GitHub Advanced Security code scanning (CodeQL) — treat AI-suggested code with the same scrutiny as human-written code. |
| 5 | Does Copilot guarantee license-safe or vulnerability-free suggestions? | No. Suggestions may match licensed public code or reproduce insecure patterns — human review is mandatory before merge. |
| 6 | What risk arises when Copilot output reflects patterns from its public training data (e.g., stereotypes in comments/names)? | Bias risk — developers must review generated comments/code for unintended bias, per Responsible AI guidance. |
| 7 | Exam trap: 'Copilot pre-vets code for security, so security review is unnecessary' | False — Copilot does not guarantee secure code. Insecure patterns (e.g., string-concatenated SQL) can still be suggested and must be reviewed/remediated. |
| 8 | Business/Enterprise vs Individual: who controls the public-code-matching filter? | Individual: user controls personal setting. Business/Enterprise: org/enterprise admin sets policy, can lock to prevent override. |
| 9 | Human-in-the-loop principle (as tested on GH-300) | Every AI suggestion must be reviewed and validated by a human before merge — accountability cannot be delegated to the AI. |
| 10 | Correct action when a Copilot suggestion matches a GPL-licensed public snippet | Remove/rewrite the code or confirm license compatibility before merging — do not merge as-is or merely credit Copilot. |
| 11 | What does 'attribution risk' mean in the context of Copilot suggestions? | Risk that a suggestion reproduces public code requiring credit or license compliance (e.g., copyleft terms) that the merging developer must satisfy. |
| 12 | What must accompany every AI-assisted code review per Responsible AI guidance? | A security review (check for vulnerable patterns) AND a licensing check (public code match) — both are heavily tested exam themes. |
