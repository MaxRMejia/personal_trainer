---
type: initiative
title: Independent Personal Trainer Website
parent: none
tracker_id: ""
key: ""
covers: [CAP-1, CAP-2, CAP-3, CAP-4, CAP-5, CAP-6]
after: []
assignee: ""
risk: high
---

# Independent Personal Trainer Website

## Description

Create a fast, accessible static website for Lynette Cruz and Regal Power Fitness so prospective clients in New Britain and nearby towns can understand services, evaluate the trainer, and contact her directly. The product spec and its companions define capabilities, content, technical constraints, and release gates.

## Outcome

Local prospects can discover Lynette Cruz, understand classes and packages, evaluate approved reviews and media, and contact her; success is the spec's mobile discovery-and-contact signal.

## Done when

1. The five required surfaces are live on Firebase Hosting and work on mobile and desktop.
2. Lynette's name, address, service area, and phone are searchable text; the listed package schedules, prices, allowances, and terms are accurate.
3. Visitors can contact Lynette directly, view approved reviews and media, and download the trainer-revised printable agreement.
4. The site passes the UX accessibility checks, including keyboard/focus, 320 CSS-pixel reflow, 200% text enlargement, and 400% zoom.
5. The site meets a performance target agreed before production release and is suitable for expected traffic below 200 visits/month on Firebase Hosting free tier.

## Boundaries

One static marketing website, its content/assets, and its Firebase Hosting deployment. No booking app, contact form, self-hosted video, or unrelated trainer operations. The one epic owns all work; the platform baseline is its opening story rather than a separate epic.

- Touch point: Firebase Hosting project/configuration — the site consumes the hosting platform; owner: epic-regal-power-fitness-website.

Tracer: entry 1 runs the shared Python, data, Jinja2, and Pillow pipeline through a Firebase preview with Home/About and Services & Classes.

## References

- spec — `_bmad-output/initiative-trainer-website/spec-personal-trainer-website/spec-personal-trainer-website.md`, Capabilities
- constraint — the same spec, Constraints and Non-goals
- UX — `_bmad-output/initiative-trainer-website/ux-personal-trainer-website/DESIGN.md` and `EXPERIENCE.md`

## Notes

- Decision: One epic owns this single website and Firebase deployment; no separate platform-baseline epic. Its foundation is the opening story (2026-10-11).
- Decision: Do not create a separate end-to-end-suite story; story-level checks and the integrated production check cover this scope (2026-10-11).
- Open question: Set a measurable performance target before production release; story 6 waits on it.
- Open question: Choose the navigation pattern before connected navigation is implemented; story 6 waits on it.
- Source conflict: the supplied agreement says to schedule through a designated booking app, while the user confirms no app exists and visitors should contact Lynette directly. The trainer will replace the PDF before publication.
- Assumption: One owner can implement the complete greenfield static site; no separate team/service boundaries exist in the repository.