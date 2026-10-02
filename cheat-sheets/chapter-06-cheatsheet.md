# Chapter 6 Cheat Sheet: Privacy & Content Exclusions

## Domain Weight
| Domain | Weight |
|---|---|
| Privacy Fundamentals and Context Exclusions | 15% |

## Plan Support Matrix
| Feature | Free/Pro (Individual) | Business/Enterprise |
|---|---|---|
| Content exclusions (org-level) | ❌ No | ✅ Yes |
| Content exclusions (repo-level) | ❌ No | ✅ Yes (if org allows) |
| Duplication-detection filter (public code match) | ❌ No | ✅ Yes |
| Prompts/suggestions used for model training | Opt-in setting exists | Never — contractual guarantee |

## Content Exclusion Levels
| Level | Who configures | Scope | Notes |
|---|---|---|---|
| Organization | Org owner | All repos matched by rule | Always enforced |
| Repository | Repo admin | Single repo | Only enforced if org policy permits repo-level config |

**Exam trap:** If org disables repo-level configuration, any existing repo-level rules are silently ignored — org-level rules still apply.

## Exclusion Rule Format (org settings, YAML-style)
```yaml
- repo:
    name: octo-org/octo-repo
    paths:
      - /secrets/**
      - /internal/**
```
Uses gitignore-style glob matching.

## What Content Exclusion Does / Does Not Do
| Does | Does Not |
|---|---|
| Blocks file content from being used as Copilot context (inline + Chat) | Hide/delete file from repo |
| Disables suggestions while editing an excluded file | Restrict git/GitHub access to the file |

## Duplication-Detection Filter
- Setting name: **Suggestions matching public code**
- Values: **Block** (filters out matches) / **Allow**
- Org-level (Business/Enterprise) setting
- Distinct from content exclusion — this is about *public* code matches, not private repo context

## Data Privacy Commitments
- Business/Enterprise: prompts & suggestions **never** used to train GitHub's underlying models (not configurable, guaranteed by default)
- Individual (Pro): optional setting — "Allow GitHub to use my code snippets for product improvements" (opt-in/out)

## Verification
- VS Code: Copilot status bar icon changes state + shows message when current file is excluded
- No official CLI command (`gh copilot exclusions verify` does **not** exist — distractor)

## Quick Memory Hooks
- **"Business protects, Individual can opt-in"** — training data rule
- **"Org sets the ceiling, repo can't exceed it"** — exclusion precedence
- **"Block = no twins"** — duplication filter prevents public-code twins in suggestions
