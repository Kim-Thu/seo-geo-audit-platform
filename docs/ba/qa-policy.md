# Per-Issue QA Policy

Every executable work issue must have one dedicated QA issue. The QA issue verifies only that work issue.

A work issue is not released to its successor until QA PASS.

QA result must record:
- checklist result
- defects with IDs/severity
- affected artifact
- required fix
- retest result
- final PASS/FAIL

QA FAIL blocks progression. Critical/High defects require rework and retest. Medium/Low may only be accepted with explicit owner, rationale and downstream impact.
