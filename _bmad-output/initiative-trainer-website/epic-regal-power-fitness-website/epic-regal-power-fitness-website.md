---
tracker_id: ""
key: ""
type: epic
title: "Regal Power Fitness Website"
parent: initiative-trainer-website
covers: [CAP-1, CAP-2, CAP-3, CAP-4, CAP-5, CAP-6]
after: []
assignee: ""
risk: high
---

# Regal Power Fitness Website

## Description

Deliver the complete static website for Lynette Cruz and Regal Power Fitness, from shared content/build foundation through all five visitor surfaces and Firebase production hosting. The personal-trainer spec and its companions are the requirement source.

## Outcome

Prospective clients across New Britain and nearby towns can discover Lynette, understand training options, evaluate approved media, and contact her; the spec's success signal is met by the live mobile-friendly site.

## Requirements

- CAP-1: Local clients can identify Lynette and her service area from searchable page text.
- CAP-2: Visitors can learn about Lynette, personal training, group classes, and packages.
- CAP-3: Visitors can evaluate the trainer through approved reviews and training media.
- CAP-4: Visitors can find the location and contact Lynette directly or through configured social profiles.
- CAP-5: Visitors can understand one-month package options and material terms.
- CAP-6: Visitors can download and print the trainer-revised agreement PDF.

## Done when

1. All five visitor surfaces are integrated and live on Firebase Hosting.
2. Trainer name, address, service towns, and phone are searchable text; classes, prices, allowances, and package policies match the source.
3. Direct contact works with real phone/email data; optional social actions appear only for real profile URLs.
4. Approved media is accessible, the revised PDF is downloadable/printable, and no obsolete agreement is published.
5. The integrated site passes the agreed mobile, accessibility, and performance checks.

## Boundaries

One greenfield static website and its Firebase Hosting deployment. No booking app, contact form, self-hosted video, or unrelated trainer operations. Story 1 owns the shared data schema, build pipeline, shell, brand assets, and Home/Services tracer. Stories 2–4 own separate gallery, contact, and review pages; story 5 extends Services after the shared contact-action handoff from story 3; story 6 integrates navigation and production release; story 7 is the cleanup-only sweep.

## References

- parent — `_bmad-output/initiative-trainer-website/initiative-trainer-website.md`
- spec — `_bmad-output/initiative-trainer-website/spec-personal-trainer-website/spec-personal-trainer-website.md`, Capabilities
- constraint — `_bmad-output/initiative-trainer-website/spec-personal-trainer-website/implementation-stack.md`
- content — `_bmad-output/initiative-trainer-website/spec-personal-trainer-website/pages-and-content.md`
- packages — `_bmad-output/initiative-trainer-website/spec-personal-trainer-website/one-month-packages.md`
- UX — `_bmad-output/initiative-trainer-website/ux-personal-trainer-website/DESIGN.md` and `EXPERIENCE.md`
- mockups — `_bmad-output/initiative-trainer-website/ux-personal-trainer-website/mockups/`

## Notes

- Tracer: story 1 proves Python → YAML/JSON → Jinja2 → Pillow WebP → Firebase preview with Home/About and Services & Classes.
- Decision: This is one website/deployment epic; the baseline is story 1, not a separate epic (2026-10-11).
- Decision: Stories 2, 3, and 4 own separate page/data files and can run in parallel after story 1; story 5 waits for the shared contact-action output from story 3 (2026-10-11).
- Decision: No separate E2E suite; story-level verification and story 6's integrated production check cover this scope (2026-10-11).
- Decision: Social links are optional and omitted until real URLs are supplied; they do not block release (2026-10-11).
- Open question: Navigation pattern remains user-deferred and must be chosen before story 6 starts.
- Open question: Agree a measurable performance target before story 6 starts.
- Unknown: Real phone/email and production Firebase settings are required before story 6 can release the site.
- Source conflict: the imported agreement's booking-app sentence conflicts with the user's direct-contact decision; the trainer's revised PDF is a release gate.
- Assumption: One owner delivers this site because the repository shows no existing team or service boundaries.