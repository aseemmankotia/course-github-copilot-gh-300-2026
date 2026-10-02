## Chapter 9 Cheat Sheet: Testing with GitHub Copilot (9% of exam)

### Core Command
| Command | Scope | Use |
|---|---|---|
| `/tests` (Copilot Chat) | Selected code / open file context only | Generates unit tests for the code in scope — NOT the whole repo |

### Feature Comparison
| Feature | Purpose | Generates Tests? |
|---|---|---|
| `/tests` | Unit test generation | Yes |
| Copilot Autofix | Remediates code-scanning/security findings | No |
| Copilot code review | Reviews PR diffs, leaves comments | No |
| Copilot Workspace | Plans/implements multi-file changes | Indirectly, if part of a plan |

### Default Coverage Gaps (heavily tested)
Copilot's default `/tests` output usually covers the **happy path only**. It commonly misses:
- Edge cases (empty string, null, zero, max length)
- Boundary values (tier transitions, off-by-one ranges)
- Invalid/malformed input
- Concurrency or async failure paths

**Fix:** Re-prompt with explicit instructions, e.g. "generate tests for empty input, max-length input, and the boundary between tier 1 and tier 2."

### False Positives — The #1 Exam Trap
A generated test can **pass while asserting nothing meaningful** (e.g., no assertion, or an assertion that's always true). This is the single most commonly missed exam concept in this domain.

**Rule:** Passing ≠ Correct. Always manually verify:
1. Does the test have a real assertion?
2. Does it fail if the implementation is broken (mutate the code mentally and check)?
3. Are edge cases represented, not just the happy path?

### Fixture / Test Data Generation
Provide type/schema definitions as context, then ask Copilot Chat to generate mock data or fixtures matching that schema. Works well for objects like `User`, `Order`, `Invoice`.

### Review-Before-Merge Checklist (exam favorite)
- [ ] Assertions present and meaningful
- [ ] Edge cases and boundaries covered
- [ ] Test data/fixtures realistic and schema-valid
- [ ] No false positives (test fails when code is intentionally broken)
- [ ] Human reviewer approved before merge — never auto-merge AI-generated tests

### Common Exam Traps
1. Assuming `/tests` output is exam-ready without review → always requires human validation.
2. Assuming full code coverage after one `/tests` run → coverage must be iteratively improved with targeted prompts.
3. Confusing `/tests` with Autofix or code review features — only `/tests` generates unit tests directly.

### Prompting Tip
Specify the test framework explicitly if not inferred correctly: "Generate these using pytest" or "using Jest."
