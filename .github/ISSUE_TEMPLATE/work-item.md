---
name: Granular Work Item
about: Smallest independently verifiable task with mandatory QA gate
---

## Task
Describe exactly one unit of work. If the task contains two independently verifiable outcomes, split it into two issues.

## Objective
Why this task exists and what risk/problem it removes.

## Inputs / Dependencies
- Previous issue(s) that must be QA PASS before this issue can start.
- Source documents / evidence / requirements used.

## Scope
### In scope
- 

### Out of scope
- 

## Actions
1. 

## Expected Result
Concrete artifact/change produced by this issue.

## Acceptance Checks
- [ ] Output exists in the expected location.
- [ ] Output contains all mandatory fields/elements for this task type.
- [ ] No unrelated work was bundled into this issue.
- [ ] Traceability IDs/dependencies are correct.
- [ ] Edge/alternate/error cases required by this task are covered.

## QA Issue
Linked QA issue: #

This work issue cannot be closed as complete until its QA issue returns PASS.

## Completion Evidence
Record after execution:
- Actual actions performed
- Artifact/file/section changed
- Result produced
- Deviations from plan
- Known limitations

## QA Result
- QA status: NOT RUN / PASS / FAIL
- Defects: 
- Retest: 

## Definition of Done
- Work completed
- Acceptance checks pass
- QA issue PASS
- Critical/High defects = 0
- Evidence recorded
- Successor issue may now start
