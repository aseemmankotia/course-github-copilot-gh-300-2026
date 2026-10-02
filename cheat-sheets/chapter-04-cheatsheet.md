# Chapter 4 Cheat Sheet: Seats, Policies, Plan Selection

## Plan Comparison
| Feature | Individual (Pro/Pro+) | Business | Enterprise |
|---|---|---|---|
| Price | $10/mo or $100/yr (Pro); $39/mo or $390/yr (Pro+) | $19/user/mo | $39/user/mo |
| Billing owner | Personal | Org | Org (within Enterprise account) |
| Seat management | N/A | Org admin assigns/removes | Org admin + enterprise policy control |
| Org policy toggles | No | Yes (public code match, chat) | Yes + enterprise-wide enforcement |
| Audit log | No | Org-level | Org-level + enterprise-wide streaming |
| Chat on github.com w/ knowledge bases | No | No | Yes |

## Seat Lifecycle
1. Admin assigns seat (UI: People > Copilot, or API `POST /orgs/{org}/copilot/billing/selected_users`)
2. User authenticates via SSO (if enforced) — seat activates on first use
3. Usage tracked; inactivity monitored
4. **90 days no activity** + auto-management enabled → seat auto-removed
5. Manual removal anytime: `DELETE /orgs/{org}/copilot/billing/selected_users`

## Key API Endpoints
| Action | Endpoint |
|---|---|
| List seats | `GET /orgs/{org}/copilot/billing/seats` |
| Add seats | `POST /orgs/{org}/copilot/billing/selected_users` |
| Remove seats | `DELETE /orgs/{org}/copilot/billing/selected_users` |
| Get billing config | `GET /orgs/{org}/copilot/billing` |

## Org-Level Policy Toggles
- **Suggestions matching public code**: Block / Allow
- **Copilot Chat** (IDE / github.com — github.com Chat is Enterprise-only feature area)
- **Copilot in the CLI**
- **Copilot in GitHub Mobile**

## Enterprise → Business Policy Inheritance (CRITICAL EXAM POINT)
| Enterprise setting | Effect on Business org |
|---|---|
| Enabled | Locked ON — org owner cannot change |
| Disabled | Locked OFF — org owner cannot change |
| No policy | Org owner sets it independently |

## SSO / SCIM (EMU)
- SSO enforcement can be required before a seat activates.
- In EMU orgs, SCIM syncs IdP group membership → team membership → Copilot seat assignment/removal automatically.

## Common Exam Traps
- Assuming org-level toggle can override a locked enterprise Enabled/Disabled policy — it cannot.
- Confusing Pro/Pro+ (individual, no org billing/policy) with Business/Enterprise (org-managed).
- Forgetting the 90-day inactivity threshold for auto seat reclamation.
- Assuming Business includes github.com Chat with knowledge bases — that's Enterprise only.
