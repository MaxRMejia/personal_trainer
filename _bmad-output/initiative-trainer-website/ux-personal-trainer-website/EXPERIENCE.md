---
name: Regal Power Fitness
status: final
sources:
  - ../spec-personal-trainer-website/spec-personal-trainer-website.md
  - ../spec-personal-trainer-website/pages-and-content.md
  - ../spec-personal-trainer-website/implementation-stack.md
  - ../spec-personal-trainer-website/one-month-packages.md
  - imports/regal_logo.jpeg
  - imports/Lynette_Cruz_One_Month_Agreement.pdf
updated: 2026-10-17
---

# Regal Power Fitness - Experience Spine

## Foundation

Mobile-first, responsive static website generated from Python, Jinja2 templates, and editable YAML/JSON content. No UI system is selected. `DESIGN.md` defines the visual identity; this document defines page structure and behavior. The [imported agreement](imports/Lynette_Cruz_One_Month_Agreement.pdf) is reference material only until the trainer supplies the revised version without the booking-app sentence. These UX documents take precedence over conflicting source visuals.

## Information Architecture

| Surface | Reached from | Purpose | Visual reference |
| --- | --- | --- | --- |
| Home/About | Site entry and site navigation | Introduce Lynette Cruz, her ISSA certification, goal-focused coaching approach, and New Britain-area service; preview the confirmed group schedule and lead visitors to packages or direct contact. | [Home/About mockup](mockups/key-home-about.html) |
| Services & Classes | Home classes/packages action and site navigation | Explain personal training by direct inquiry, group schedule, packages, material terms, and the agreement download beneath the shared navigation and a spacious page-intro band. | [Services & Classes mockup](mockups/key-services-classes.html) |
| Reviews | Site navigation | Present trainer-approved review screenshots beneath the shared navigation and a spacious page-intro band. | [Reviews mockup](mockups/key-reviews.html) |
| Media Gallery | Site navigation | Present photos and embedded YouTube/Instagram videos beneath the shared navigation and a spacious page-intro band. | [Media Gallery mockup](mockups/key-media-gallery.html) |
| Contact/Location | Site navigation and contact actions | Show the confirmed address, service towns, and phone/email/social contact actions beneath the shared navigation and a spacious page-intro band. | [Contact/Location mockup](mockups/key-contact-location.html) |

All five surfaces are required and reachable through the primary navigation: Home, Services, Media Gallery, Reviews, and Contact Us. Use the same shared navigation component and markup on every page, changing only the active-page state. Its styles live in [site-navigation.css](mockups/site-navigation.css), linked by all five mockups. Use horizontal links on desktop and a compact expandable menu on mobile. Indicate the current page. The Home primary action leads to Services & Classes.

Keep the primary navigation focused on page destinations. Do not repeat a phone-call link in the Home navigation; direct-call actions belong in the Home content and Contact surface.

The [imported logo](imports/regal_logo.jpeg) is the brand reference for every surface; its embedded lettering does not replace searchable page text.

The Home/About content uses Lynette-approved copy: ISSA Certified; personal and group training; workouts tailored to a client's goals and varied from session to session; careful attention to form and body mechanics; and a motivating coaching style. Use these themes as original site copy, not as a quotation or a promise of individual results. Do not identify or imply affiliation with another gym.

## Voice and Tone

Use high-energy, motivational, direct language. Keep schedule, package, and agreement copy factual and consistent with trainer-approved terms. Avoid guarantees about fitness outcomes.

| Do | Don't |
| --- | --- |
| Use concise, active invitations to explore classes and contact Lynette. | Invent claims, prices, schedule details, or booking methods. |
| State direct-contact steps plainly. | Suggest that a booking app or contact form exists. |
| Use readable, factual package terms. | Hide cancellation, expiration, or payment terms in promotional copy. |

## Component Patterns

| Component | Use | Behavioral rules |
| --- | --- | --- |
| page-surface | All surfaces | Keep primary reading content on the light base surface. |
| brand-band | Home/About and section breaks | Use only for brand emphasis; retain readable text contrast. |
| brand-band-copy | Dark bands | Keep body copy white and readable; do not put essential details in logo art. |
| page-intro | Services & Classes, Reviews, Media Gallery, Contact/Location | Give the page title and short orientation copy a generous vertical band below the shared navigation; retain at least 250 px height on mobile. |
| secondary-copy | Supporting details | Use for captions and metadata that remain legible at zoom. |
| brand-accent-text | Labels and small highlights | Use dark gold only on light surfaces. |
| divider | Related content rows | Separate package or contact details without adding nested cards. |
| home-classes-packages-action | Home/About | Navigate to Services & Classes. |
| contact-action | Home, Services & Classes, Contact/Location | Phone/email actions contact Lynette directly; social actions appear only when real profile URLs are supplied. No booking-app destination. |
| agreement-download | Services & Classes | Download the revised PDF for saving/printing only after the trainer replaces the current file and removes the obsolete app-booking sentence. |
| package-comparison | Services & Classes | Expose package price, schedule, allowance, and terms without requiring a hidden interaction. |
| video-embed | Media Gallery | Load the requested embeds immediately when the gallery loads; provide accessible titles. |
| review-image | Reviews | Use supplied screenshots only after source and reuse permission are confirmed; provide useful alternative text. |
| brand-logo | All surfaces | Use the supplied mark; keep trainer name, service area, and phone as separate text. |
| trainer-photo | Home/About | Use Lynette's approved original after the background edit; do not publish the low-resolution gym screenshot or show another business's signage/apparel. |
| site-navigation | All surfaces | Keep the five primary page links consistent on every surface, indicate the current page, and use a compact disclosure menu on mobile. Links and the menu control provide at least 44 px touch targets. |

## State Patterns

| State | Surface | Treatment |
| --- | --- | --- |
| Contact detail missing | Contact/Location | Keep explicit content placeholders in data, do not render nonfunctional links as live contact actions, and block launch until a real phone or email destination is configured. |
| Social URL missing | Contact/Location | The supplied profile names may appear as plain text; omit active links until Lynette confirms exact profile URLs. Never link to `#` or a placeholder URL. |
| Revised agreement missing | Services & Classes | Do not publish the existing PDF; block launch until the trainer supplies the revised file with the obsolete booking-app sentence removed. Enable the download only then. |
| Trainer photo pending | Home/About | Keep the photo area as a clearly identified placeholder until Lynette approves the original/background edit. Do not publish the low-resolution screenshot or imagery that reveals another gym's branding. |
| Approved photography missing | Media Gallery | Do not invent or publish stock imagery as trainer photography; final photo direction/assets remain open. |
| Review screenshot permission missing | Reviews | Do not publish unapproved screenshot content; obtain source and reuse permission first. |
| Review screenshot unavailable | Reviews | Do not show a broken image; show its approved text equivalent or omit the review until the asset is restored. |
| Gallery photo unavailable | Media Gallery | Omit the broken image and preserve any available caption or description. |
| Video embed unavailable | Media Gallery | Show a concise unavailable message and a direct provider link when its URL is configured; do not leave an indefinite loading state. |

## Interaction Primitives

- Use standard links for page navigation and direct contact; phone and email actions use their corresponding device handlers when real details are configured.
- Lynette's phone (`860-391-9726`) and email (`lynettecruz@hotmail.com`) are confirmed and may render as active `tel:` and `mailto:` links. Social handles are known, but URLs remain pending and are not clickable yet.
- Provide a skip link, visible unobscured keyboard focus, logical tab order, descriptive page titles, and keyboard-operable navigation. The mobile menu opens and closes with its native disclosure control; following a link navigates to that page.
- Ensure interactive targets meet WCAG 2.2 minimum target size or its spacing exception; navigation links and its menu control are at least 44 px, and primary actions are at least 48 px high.
- Do not introduce a booking app, online registration flow, or contact form in this phase.
- The agreement action downloads a static PDF; the file must be the trainer-updated version.
- Video embeds load immediately as already decided; include descriptive iframe titles and do not self-host video.
- All links and controls work by keyboard, show visible focus, and have descriptive accessible names.

## Accessibility Floor

- Meet WCAG 2.2 AA for text contrast, focus visibility, keyboard operation, and image alternatives.
- Verify no content loss or two-dimensional scrolling at 320 CSS px and at 400% zoom from a 1280 CSS px viewport; verify text at 200% enlargement does not clip or lose functionality.
- Keep the trainer name, address, service area, and phone as selectable text, not image-only content.
- Preserve logical heading order, landmarks, page titles, and reading order across all five surfaces.
- Ensure package information remains understandable on narrow screens and at zoomed text sizes.
- Give the logo concise alternative text only when adjacent text does not repeat it. Make review text, rating, and attribution available in the reading flow instead of relying on screenshot alt text alone.
- Give review images meaningful alternatives; videos have descriptive titles, keyboard-operable native controls, and captions or equivalent access to meaningful prerecorded speech.
- Before publishing the agreement, verify selectable text, document tags and reading order, and understandable printed fields/signature areas.

## Key Flows

### Flow 1 - Explore a package and contact Lynette (Alex, illustrative local prospect; CAP-2, CAP-4, CAP-5, CAP-6)

Visual references: [Home/About](mockups/key-home-about.html), [Services & Classes](mockups/key-services-classes.html).

1. Alex arrives at Home/About and sees Lynette Cruz, her ISSA certification, goal-focused training approach, the New Britain-area service region, and her trainer-photo placeholder.
2. Alex follows the classes/packages action to Services & Classes.
3. Alex compares the Tuesday/Thursday and Saturday options, including price, allowance, and material terms.
4. Alex downloads and reviews the trainer-updated agreement when the corrected PDF is available.
5. Alex uses the confirmed phone or email action to contact Lynette directly and ask to register; no app is involved.
6. **Climax:** Lynette receives Alex's inquiry with the selected class/package as context.

**Failure:** If phone/email values are placeholders, omit active contact links and block launch. If the revised PDF is missing, omit its download and block launch.

The protagonist is illustrative; audience demographics and navigation presentation remain open. The final trainer photo remains pending. The flow cannot complete before real contact details and the revised agreement are supplied.

### Flow 2 - Evaluate training and verify local fit (Jordan, nearby prospect; CAP-1, CAP-3, CAP-4)

Visual references: [Reviews](mockups/key-reviews.html), [Media Gallery](mockups/key-media-gallery.html), [Contact/Location](mockups/key-contact-location.html).

1. Jordan opens Home/About and reads the trainer name, service area, and primary classes/packages route.
2. Jordan opens Reviews and reads approved review text with its screenshot, rating, and attribution.
3. Jordan opens Media Gallery and views trainer-approved photos or plays an embedded video with available captions.
4. Jordan opens Contact/Location and confirms the address and service towns match their area.
5. Jordan uses a configured phone, email, or social profile action to contact Lynette directly.
6. **Climax:** Jordan reaches Lynette with enough local and service context to ask about a suitable training option.

**Failure:** Apply the media and missing-profile fallbacks in State Patterns. If direct-contact details are missing, omit the action and block launch.

## Responsive & Platform

Build for mobile first, then widen the content layout for larger screens without scaling type by viewport width. Keep the package comparison readable as a stacked layout on small screens. Use platform-native telephone and email handlers from accessible links.

## Open Inputs

- Lynette's original trainer photo with the updated background and review-image reuse permission are not yet supplied.
- Phone and email are confirmed; exact URLs for the supplied Instagram, Snapchat, and Facebook accounts are still needed before making social links active.
- The trainer must provide the revised agreement PDF before the download action can be published.
- Confirm caption availability for selected videos and privacy information for immediate third-party embeds.