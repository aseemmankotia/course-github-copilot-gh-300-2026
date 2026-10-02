## Chapter 11 Cheat Sheet: Cross-Domain Scenario Drills

### Plan Feature Matrix
| Feature | Individual/Pro | Business | Enterprise |
|---|---|---|---|
| Chat (IDE/github.com) | Yes (limited) | Yes | Yes |
| Content exclusion (path-based) | No | Yes (org-level) | Yes (org + enterprise-wide) |
| Public code matching filter | Fixed default | Toggleable, org-level | Toggleable, enterprise-wide |
| Knowledge Bases | No | No | Yes |
| Centralized policy across multiple orgs | No | No | Yes |
| Autofix (security remediation) | N/A | With Advanced Security | With Advanced Security |

### Privacy & Data Handling Rules
- **Content exclusion**: hides files/paths from Copilot context AND suggestions. Business/Enterprise only. Configured via org settings using gitignore-style patterns.
- **Public code matching filter**: blocks completions duplicating ≥150 characters of known public code. Addresses license/IP risk, NOT security vulnerabilities.
- **Model training**: Business/Enterprise prompts/suggestions are not used to train GitHub's models. Individual has a personal opt-in/out setting.
- Do not confuse: Content exclusion (privacy of source) vs. Public code filter (output license risk) vs. Autofix (security remediation).

### Responsible AI / Testing Checklist
1. AI-generated code (completions, Autofix, Chat) always requires **human review** before merge.
2. Automated tests supplement but do not replace human review.
3. Hallucination risk: verify unfamiliar APIs/library calls Copilot suggests.
4. License risk: rely on the public code matching filter, but still review flagged suggestions.

### Prompt Engineering Quick Rules
- Descriptive comments above code = better completions.
- Keep related files open — Copilot uses open-file context.
- Vague/short prompts → vague/low-quality output.
- Multi-file context improves relevance; don't disable it.

### Scenario Question Strategy (Time Management)
- Read the full requirement list FIRST — note every constraint (plan tier, scale, cost, privacy, security).
- Eliminate options violating any single constraint immediately.
- When two options both look valid, choose the one meeting **all** stated constraints, not just most.
- Watch for scope traps: "single org" vs. "multiple orgs/enterprise-wide" changes the correct plan answer.
- Don't overthink conceptual questions — they map to one clear documented fact; move on quickly if unsure and flag for review.
