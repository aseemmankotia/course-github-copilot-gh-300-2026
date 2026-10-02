## Copilot Plans Cheat Sheet

### Plan Overview
| Plan | Billed To | Price | Seat Mgmt |
|---|---|---|---|
| Free | Personal account | $0 | N/A |
| Pro | Personal account | $10/mo or $100/yr | Self |
| Pro+ | Personal account | $39/mo | Self |
| Business | Organization | $19/user/mo | Org admin |
| Enterprise | Enterprise account | $39/user/mo | Org/enterprise admin |

### Usage Limits
| Plan | Completions | Chat | Premium Requests/mo |
|---|---|---|---|
| Free | 2,000/mo | 50 msgs/mo | 0 |
| Pro | Unlimited | Unlimited | 300 |
| Pro+ | Unlimited | Unlimited | 1,500 |
| Business | Unlimited | Unlimited | 300/user |
| Enterprise | Unlimited | Unlimited | 1,000/user |

### Feature Matrix
| Feature | Free | Pro | Pro+ | Business | Enterprise |
|---|---|---|---|---|---|
| Completions | ✅ (capped) | ✅ | ✅ | ✅ | ✅ |
| Chat (IDE) | ✅ (capped) | ✅ | ✅ | ✅ | ✅ |
| Chat on github.com | ❌ | Limited | Limited | ✅ | ✅ |
| CLI | ✅ | ✅ | ✅ | ✅ | ✅ |
| PR Summaries | ❌ | ❌ | ❌ | ✅ | ✅ |
| Org-level Policies | ❌ | ❌ | ❌ | ✅ | ✅ |
| Enterprise-wide Policies (multi-org) | ❌ | ❌ | ❌ | ❌ | ✅ |
| Knowledge Bases | ❌ | ❌ | ❌ | ❌ | ✅ |
| Audit Log Events | ❌ | ❌ | ❌ | ✅ | ✅ |
| IP Indemnification | ❌ | ❌ | ❌ | ✅ | ✅ |

### Decision Rules (Exam Logic)
- **Personal, unmanaged, unlimited completions** → Pro or Pro+ (Pro+ if heavy premium model use).
- **Org needs seat control + policies + audit log, no knowledge bases** → Business.
- **Multiple orgs need unified policy, OR need Knowledge Bases** → Enterprise (requires GitHub Enterprise Cloud).
- **PR summaries or Chat-on-github.com requirement mentioned** → rules out Free/Pro/Pro+; requires Business or Enterprise.

### Common Traps
- Assuming Pro/Pro+ has org policy controls — it never does.
- Confusing Business's 300 premium requests/user with Enterprise's 1,000/user.
- Assuming Business includes Knowledge Bases — it does not; that's Enterprise-exclusive.
- Forgetting Enterprise requires GitHub Enterprise Cloud as a prerequisite.
