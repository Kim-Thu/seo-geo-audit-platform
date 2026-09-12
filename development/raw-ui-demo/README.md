# Raw UI Demo Sandbox (Astro)

This folder exists to turn BA → DA → UI/UX decisions into **fast visual checkpoints** before production implementation.

It is intentionally separate from the future `apps/web` Next.js application.

## Purpose

Use this sandbox to answer visual questions early:
- Is information hierarchy clear?
- Is the dashboard too dense or too empty?
- Can users scan issue severity/priority/evidence quickly?
- Are UNKNOWN / PARTIAL / FAILED / STALE states understandable?
- Does the issue → task → validation loop make sense when rendered as screens?
- Do Website Overview, Crawl, Issues, Search and GEO feel like one product?

Do **not** use it to redefine product semantics.

## Run locally

```bash
cd development/raw-ui-demo
npm install
npm run dev
```

Then open the local Astro URL shown in the terminal.

## Current routes

- `/` — demo index
- `/website-overview`
- `/crawl`
- `/issues`
- `/page-detail`
- `/search`
- `/geo`
- `/tasks`

The current routes are intentionally raw placeholders. Replace each route with the specific layout being discussed.

## Traceability rule

Every demo screen must include a trace note. Minimum useful trace:

```text
BA: FR / UC / business rule
DA: entity / metric / DC-* contract
UIUX: FLOW-* / SCR-* / STATE-* / CMP-*
```

Example:

```text
BA: UC-003 Review SEO Issue
DA: DC-ISSUE-LIST / DC-ISSUE-DETAIL
UIUX: SCR-IssueList / SCR-IssueDetail / STATE-PARTIAL
```

Dummy data is allowed, but field names, lifecycle states and metric meanings must come from approved artefacts.

## Prototype rules

1. This is visual validation, not production implementation.
2. Do not add real authentication, database, queue, crawler or provider integration here.
3. Do not create a generic SEO/GEO score.
4. Keep `0`, `NULL`, `UNKNOWN`, `PARTIAL`, `FAILED` and `STALE` semantically distinct.
5. `Task Done` does not mean `Issue Closed`; validation evidence still controls closure.
6. AI mention and AI citation are separate observations.
7. If a prototype reveals a semantic gap, update BA/DA/UIUX through change control before production code.
8. Visual-only changes can later inform `DEV-IMP-*` implementation without changing upstream semantics.

## Suggested iteration method

For each screen discussion:

```text
1. Identify upstream BA/DA/UIUX IDs.
2. Copy the closest raw route or component.
3. Add realistic dummy data matching the contract.
4. Test desktop + mobile information hierarchy.
5. Compare alternatives if needed.
6. Record findings in the related GitHub issue/comment.
7. If semantics changed, return to change control.
8. If visual direction is accepted, carry it into production implementation later.
```

## GitHub tracking

Primary setup issue: #1 — `[DEV-RAW] Astro raw UI demo sandbox for BA/DA/UIUX visual validation`.

The project Work Tracker should keep sandbox bootstrap and ongoing visual checkpoints separate from production `DEV-IMP-*` progress.
