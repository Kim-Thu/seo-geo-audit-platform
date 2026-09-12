# Strict Progression Policy

No parallel execution inside a sequential BA work package unless explicitly approved by dependency analysis.

State flow:
Not Started -> Ready -> In Progress -> Ready for QA -> QA PASS -> Released.
If QA FAIL: In Progress -> Ready for QA -> QA FAIL -> Rework -> Retest -> QA PASS.

Only QA PASS releases the successor issue.
