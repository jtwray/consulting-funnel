# Consulting Funnel · paid-work acquisition system

**Status:** planning and design package, not a deployed application.  
**Prepared:** 2026-10-23 · America/New_York  
**Canonical repository:** [`jtwray/consulting-funnel`](https://github.com/jtwray/consulting-funnel).  
**Original archive:** [`jtwray/dashboarda` draft PR #3](https://github.com/jtwray/dashboarda/pull/3), under `docs/consulting-funnel/`.

## Purpose

Turn the recurring Paid Engineering Gig Radar from a chronological chat feed into a **measurable customer-acquisition funnel**: find real, paid, suitable engineering tasks; assess scope and buyer quality; create truthful proposals with defensible evidence; record approved submissions and replies; win work; deliver; and learn what converts. Keep this **separate from the W2/full-time employment search**.

**North star:** collected net consulting/freelance revenue per total hour spent acquiring *and delivering* work, interpreted alongside reputation and repeat-business outcomes. Early on, prioritize first paid contract and proposal-to-reply conversion while avoiding misleading conclusions from tiny samples.

## Package contents

- [`ROADMAP.md`](ROADMAP.md): stages, priorities, cross-repo responsibility, dependencies, review gates.
- [`DECISIONS.md`](DECISIONS.md): ten recorded product decisions and caveats.
- [`specs/OPPORTUNITY-SCHEMA.md`](specs/OPPORTUNITY-SCHEMA.md): field contract, provenance, canonical ID, status transitions.
- [`specs/SCORING-AND-EXPERIMENTS.md`](specs/SCORING-AND-EXPERIMENTS.md): initial weights, exclusions, timing study, measurement.
- [`specs/SAFETY-AND-AUTOMATION.md`](specs/SAFETY-AND-AUTOMATION.md): human approvals, platform-specific allowlists, controls.
- [`slices/`](slices/): implementation-agent-ready boundaries, evidence and independent reviewer acceptance criteria.
- [`visuals/`](visuals/): eight editable SVG recreations, accessible descriptions, Markdown table counterparts, with PNG previews in the original local ZIP (not tracked in this repository).

## Relationship to Dashboarda

`jtwray/dashboarda` already hosts small Netlify apps and a private dashboard reader/upserter. Existing `job-rates` is **not** the same as this opportunity pipeline. The connected dashboard interface currently exposes only its existing dashboard allowlist. `gig-radar` **must be explicitly wired, authorized, tested and deployed** before any scheduler can upsert into it. Do not claim this integration is already live.

The preferred ownership split is **this repo for product/business process, decisions, funnel analysis, visualization assets and slice contracts**; **Dashboarda for executable `apps/gig-radar`, storage, UI, integration and deployment**. Links in both directions, no duplicate authoritative roadmap. This repository is the canonical home for the product roadmap. The earlier Dashboarda draft PR is retained as provenance, not a second authoritative roadmap.

## What is not done

No new gig-radar app has been implemented. No scheduled gig-ingestion-to-Dashboarda sync has been enabled. No automatic bidding/submission has been implemented. No clients have been contacted by this package.

## Next step

Approve the naming/ownership and S1 scope, then dispatch a single-use development agent from [`slices/S1-PERSISTENT-QUEUE.md`](slices/S1-PERSISTENT-QUEUE.md); run an independent acceptance review before merging. Original sources must be collected lawfully, and application submission remains human-approved.
