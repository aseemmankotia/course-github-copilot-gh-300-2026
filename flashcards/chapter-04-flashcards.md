## Chapter 4: Seat Management, Org Policies, and Plan Selection Scenarios — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Copilot Business price per seat/month? | $19/user/month. Exam tip: billed monthly through the org, requires an admin to assign seats. |
| 2 | Copilot Enterprise price per seat/month? | $39/user/month. Adds audit log streaming, knowledge bases, and Copilot Chat on github.com vs Business. |
| 3 | Copilot Pro (individual) pricing? | $10/month or $100/year. Purchased personally, not org-managed — no centralized policy or billing. |
| 4 | Copilot Pro+ (individual) pricing? | $39/month or $390/year. Higher premium request allowance than Pro; still an individual consumer plan, not org/enterprise. |
| 5 | Inactive seat auto-removal threshold? | 90 days of no Copilot activity, if automatic seat management is enabled by the admin. |
| 6 | Three possible states for an enterprise-level Copilot policy? | Enabled, Disabled, or No policy. Enabled/Disabled lock the setting for all child orgs; No policy delegates the choice to org owners. |
| 7 | Business vs Enterprise: which tier supports knowledge-base-grounded Copilot Chat on github.com? | Enterprise only. Business supports IDE Chat but not org-knowledge-grounded Chat on github.com. |
| 8 | API endpoint to add Copilot seats to specific users in an org? | POST /orgs/{org}/copilot/billing/selected_users — used for programmatic seat assignment instead of the UI. |
| 9 | API endpoint to remove Copilot seats from specific users? | DELETE /orgs/{org}/copilot/billing/selected_users — triggers seat reclamation and stops billing for those users. |
| 10 | API endpoint to list current Copilot seat assignments in an org? | GET /orgs/{org}/copilot/billing/seats — returns each assigned user, assigning team, and last activity date. |
| 11 | In an EMU org, how are Copilot seats typically managed? | Via SCIM group sync — adding/removing a user from the mapped IdP group automatically assigns/removes their Copilot seat. |
| 12 | Which policy toggle controls whether Copilot completions can echo code identical to public repos? | 'Suggestions matching public code' — set to Block or Allow at org level (or inherited/locked from enterprise). |
