# Responsible AI & Ethical Use of Copilot — Cheat Sheet (Domain weight: 7%)

## Core Principle: Human Accountability
| Statement | Exam Truth |
|---|---|
| Copilot suggests, human decides | Developer who merges is accountable — always |
| "Copilot's fault" is a valid excuse | FALSE — never accepted on exam |
| AI suggestions require review before merge | TRUE — mandatory, not optional |

## Licensing & Attribution Risk
| Concept | Detail |
|---|---|
| Public code matching | Copilot may output snippets resembling public repo code |
| Risk | Matched code may carry license terms (e.g., GPL, attribution) |
| Mitigation setting | **Suggestions matching public code** — Block or Allow |
| Individual plan | User controls setting personally |
| Business/Enterprise | Admin sets policy at org/enterprise level; can be locked |
| Correct remediation | Rewrite/remove matched code or verify license compatibility — do NOT just credit Copilot |

## Security Review of AI Suggestions
| Concept | Detail |
|---|---|
| Assumption to avoid | "Copilot suggestions are pre-vetted for security" — FALSE |
| Common vulnerable pattern | String-concatenated SQL queries, hardcoded secrets |
| Recommended tool | GitHub Advanced Security code scanning (CodeQL) in CI |
| Secret exposure | Use secret scanning / push protection alongside review |
| Review standard | Same rigor as human-written code — no exceptions for AI origin |

## Bias Awareness
| Concept | Detail |
|---|---|
| Source of bias | Public training data may reflect stereotypes/assumptions |
| Where it appears | Comments, variable names, example data, default assumptions |
| Required action | Reviewer identifies and corrects biased output |

## Responsible AI Pillars (applied to pair programming with Copilot)
- Human accountability (final responsibility rests with the developer)
- Fairness (review for bias in generated content)
- Reliability & security (treat suggestions as unverified until reviewed/scanned)
- Transparency (disclose AI assistance where organizationally required)

## Quick Decision Rules
- Suggestion matches public code → verify license → rewrite if uncertain
- Suggestion has insecure pattern → fix before merge, run code scanning
- Suggestion has biased language → rewrite, don't merge as-is
- Bug traced to AI-suggested code → developer/org accountable, not GitHub

## Common Exam Traps
1. Believing GitHub/Copilot bears legal or security liability — it does not.
2. Assuming 'Suggestions matching public code = Blocked' guarantees zero licensing risk — it reduces but does not eliminate risk; human review still required.
3. Thinking security scanning replaces code review — scanning supplements, not substitutes, human validation.
