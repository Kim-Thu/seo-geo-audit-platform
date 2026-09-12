# BA Execution Rule

BA work is executed as the smallest independently verifiable issue.

Rules:
1. One work issue = one independently verifiable outcome.
2. Every work issue has exactly one linked QA issue.
3. A successor work issue starts only after predecessor QA = PASS.
4. QA FAIL creates explicit defect/rework issue(s) and requires retest in the originating QA issue.
5. Parent work-package issues are containers only and never count as completion evidence.
6. Project Control is the source of truth for status/progress/dependency; GitHub is the operational audit trail.
7. Critical/High QA defects block progression.
8. Document existence is not completion.
