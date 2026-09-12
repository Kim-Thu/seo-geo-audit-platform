# Raw UI Demo Sandbox (Astro)

This folder turns BA → DA → UI/UX decisions into **populated visual checkpoints** before production implementation.

It is intentionally separate from the future `apps/web` Next.js application.

## Purpose

This is not a blank wireframe gallery. Every route should look close enough to a real operational product that we can judge:
- information hierarchy;
- data density;
- scanability;
- relationship between summary → evidence → action;
- clarity of partial / stale / failed states;
- whether BA/DA/UIUX assumptions still make sense after real content is placed on screen.

A useful prototype may expose that the existing UI/UX specification is wrong or incomplete. That is expected. Record the finding and correct the upstream spec before production implementation.

## Run locally

```bash
cd development/raw-ui-demo
npm install
npm run dev
```

## Current populated routes

- `/` — visual validation workspace
- `/website-overview` — north-star operational dashboard
- `/crawl` — crawl progress, history and partial/failure diagnostics
- `/issues` — issue inventory with severity, priority and lifecycle
- `/page-detail` — URL snapshot, indexability, issues, CWV and search evidence
- `/search` — query performance and opportunities
- `/geo` — AI mentions, citations, source gaps and run observations
- `/tasks` — remediation queue and evidence-driven validation

## Traceability rule

Every demo screen must include a trace note. Minimum useful trace:

```text
BA: FR / UC / business rule
DA: entity / metric / DC-* contract
UIUX: FLOW-* / SCR-* / STATE-* / CMP-*
```

Dummy data is allowed and encouraged for visual validation, but lifecycle states and metric meanings must match the approved/active contracts.

## Prototype rules

1. This is visual validation, not production implementation.
2. Populate screens with realistic content; blank boxes are not sufficient validation.
3. Do not add real authentication, database, queue, crawler or provider integration here.
4. Do not create a generic SEO/GEO score.
5. Keep `0`, `NULL`, `UNKNOWN`, `PARTIAL`, `FAILED` and `STALE` semantically distinct.
6. `Task Done` does not mean `Issue Closed`; validation evidence still controls closure.
7. AI mention and AI citation are separate observations.
8. If the populated layout exposes a semantic or flow gap, amend BA/DA/UIUX through change control.
9. If the problem is visual-only, update this prototype first and later carry the accepted pattern into `DEV-IMP-*`.
10. Do not mark production implementation tasks Done because a raw Astro screen exists.

## Review questions per screen

- In 5–10 seconds, can the user tell what needs attention?
- Is the primary action obvious without hiding evidence?
- Are KPIs source/freshness/completeness aware where required?
- Does the screen distinguish fact, derived metric, heuristic and recommendation?
- Can the user drill from summary to evidence without losing context?
- Are tables readable at realistic row/column density?
- Are partial/error/empty states understandable?
- Does the screen still work when values are long, zero, null or unavailable?
- Does mobile/responsive behavior preserve priority order rather than simply stacking everything?

## Iteration method

```text
1. Pick an upstream workflow/screen.
2. Load realistic dummy content shaped like the data contract.
3. Render a complete operational screen, not a skeleton.
4. Review hierarchy, density, actions, states and drill-down path.
5. Record visual issues separately from semantic issues.
6. Fix visual-only problems in Astro.
7. For semantic gaps, update the relevant UI/UX/DA/BA artefact through change control.
8. Only accepted patterns move into future production implementation.
```

## GitHub tracking

Primary issue: #1 — `[DEV-RAW] Astro raw UI demo sandbox for BA/DA/UIUX visual validation`.

Project Control tracks bootstrap, populated visual checkpoints and upstream UI/UX correction separately from production `DEV-IMP-*` progress.
