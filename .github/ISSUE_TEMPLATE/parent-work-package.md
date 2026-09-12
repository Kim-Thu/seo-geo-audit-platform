---
name: Parent Work Package
about: Non-executable container for granular work issues and QA gates
---

## Purpose
Group one coherent work package. This issue is NOT executable work and cannot be used as evidence that the package is complete.

## Scope
Describe package boundary and downstream consumer.

## Child Work Sequence
List the smallest work issues in strict order. Each child must have its own QA issue.

| Order | Work Issue | QA Issue | Start Condition | Release Condition |
|---|---|---|---|---|

## Package Exit Criteria
- [ ] Every child work issue complete.
- [ ] Every child QA issue PASS.
- [ ] All Critical/High defects closed and retested.
- [ ] Package integration QA PASS.
- [ ] Project Control matches GitHub state.

## Rule
Parent issue never substitutes for child execution or QA. The next work package cannot start until this parent package receives final integration PASS.
