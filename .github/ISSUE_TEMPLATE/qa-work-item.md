---
name: QA for Work Item
about: Mandatory independent QA for one granular work issue
---

## QA Target
Work issue: #

## QA Objective
Verify only the output of the linked work issue. Do not combine QA for multiple independently verifiable work issues.

## Preconditions
- [ ] Linked work issue execution is finished and evidence is recorded.
- [ ] Required artifact/version is available.

## QA Checks
### Completeness
- [ ] All in-scope actions were actually completed.
- [ ] Expected output exists.
- [ ] Mandatory elements are present.

### Correctness
- [ ] Output matches the task objective and source requirements.
- [ ] No unsupported assumptions were introduced.
- [ ] Dependencies and IDs are correct.

### Boundary / Edge Checks
- [ ] Out-of-scope work did not leak into the result.
- [ ] Required alternate/error/edge conditions are represented where applicable.
- [ ] No contradiction with already QA-approved predecessor artifacts.

### Traceability
- [ ] Inputs can be traced backward.
- [ ] Output can be consumed by the declared successor task.
- [ ] Evidence/references are recorded.

## Defects
Use one row per defect:

| Defect ID | Severity | Finding | Expected | Actual | Required Fix | Status | Retest |
|---|---|---|---|---|---|---|---|

## QA Decision
- [ ] PASS — successor issue may start.
- [ ] FAIL — successor remains blocked; open/reuse rework issue and retest this QA.

## Exit Rule
PASS only when Critical/High defects = 0 and every mandatory check passes. Closing this QA issue is the explicit release signal for the next work issue.
