---
id: SPEC-personal-trainer-website
companions:
  - pages-and-content.md
  - implementation-stack.md
  - one-month-packages.md
sources: []
---

# Independent Personal Trainer Website

## Why

Local prospective clients need a clear way to discover Lynette Cruz and Regal Power Fitness in New Britain, Connecticut, understand personal training and group-class offers, evaluate credibility, and make contact. The audience includes people in nearby Connecticut cities and towns as well as New Britain residents.

## Capabilities

- **CAP-1**
  - **intent:** Prospective clients in New Britain and nearby Connecticut communities can identify the trainer and service area.
  - **success:** Lynette Cruz, the service area, and phone are visible as searchable text, not embedded in images.
- **CAP-2**
  - **intent:** Prospective clients can learn about Lynette Cruz, personal-training sessions, group classes, and packages.
  - **success:** Home/About and Services & Classes present the trainer profile, contact-led personal training, current group schedule, and package options.
- **CAP-3**
  - **intent:** Prospective clients can evaluate the trainer through reviews and training media.
  - **success:** Reviews presents review screenshots, and Media Gallery presents photos and embedded YouTube or Instagram videos.
- **CAP-4**
  - **intent:** Prospective clients can find the trainer and initiate contact through direct and social channels.
  - **success:** Contact/Location displays 1 Hartford Square, New Britain, CT 06052 as searchable text, provides phone and email actions, and includes editable profile links or placeholders for Instagram, Facebook, TikTok, Snapchat, X, YouTube, and LinkedIn.
- **CAP-5**
  - **intent:** Prospective clients can understand one-month package options and material class-pack terms before making an inquiry.
  - **success:** Package content presents trainer-confirmed prices, class allowances, schedules, booking requirements, and material policies.
- **CAP-6**
  - **intent:** Prospective clients can save and print the one-month agreement.
  - **success:** A visible agreement download button downloads the supplied PDF from the static site, and the PDF can be printed.

## Constraints

- Trainer identity, service area, and phone must be rendered as real text for local search; temporary placeholders must be replaceable through content data.
- The confirmed street address, 1 Hartford Square, New Britain, CT 06052, must be editable and rendered as searchable Contact/Location text.
- The supplied Regal Power Fitness logo and its red, black, and gold colors define the brand direction.
- Target New Britain and the nearby Connecticut communities Plainville, Southington, Newington, West Hartford, Bristol, and Berlin.
- Social profile placeholders cover Instagram, Facebook, TikTok, Snapchat, X, YouTube, and LinkedIn; final URLs must come from the trainer.
- The supplied agreement PDF must be included in deployed static assets and linked from a visible download control.
- The site must be mobile-first, accessible, and fast.
- Trainer information must be updateable in content data without editing HTML templates.

## Non-goals

- A contact form is outside this phase; contact is by phone and email buttons.
- Self-hosting video is outside scope; videos are embedded from their platforms.

## Success signal

A prospective client on a mobile device can identify Lynette Cruz and the New Britain-area service region, understand personal-training and group-class packages, view trust-building reviews or media, initiate contact by phone, email, or a confirmed social profile, and download and print the agreement. The generated static site can be deployed to Firebase Hosting within the free tier for expected traffic below 200 visits per month.

## Assumptions

- Trainer-specific personal and business details use clearly identifiable placeholders until the trainer supplies final information.

## Open Questions

- The supplied PDF package title says Tuesday & 3rd Thursday, while the confirmed schedule is Tuesday and Thursday. Should the downloadable PDF be corrected before publication, or offered unchanged?
- What is the designated booking app and public URL, and should the site link to it?
- What bio, credentials, phone/email, photos, review screenshots with reuse permission, and video URLs should be supplied? Which social profile URLs should replace the placeholders when available?
- Is anything else in scope, such as a map, privacy information for embedded media, analytics, or other conversion flows?