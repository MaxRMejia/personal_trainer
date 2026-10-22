# Accessibility Review — Secondary Pages

## Scope

Reviewed `mockups/key-media-gallery.html`, `mockups/key-reviews.html`, `mockups/key-contact-location.html`, `mockups/site-secondary-pages.css`, and the shared `mockups/site-theme.css` / `mockups/site-navigation.css`. Compared shared navigation, focus, motion, and color behavior with the existing Services & Classes page. The earlier `review-accessibility.md` was left unchanged.

## Findings

### Moderate — Move keyboard focus to the skip-link destination

- **Location:** `mockups/key-media-gallery.html:50`, `mockups/key-reviews.html:50`, `mockups/key-contact-location.html:50`; corresponding skip links at line 15 of each file.
- **Evidence:** Each skip link targets `#main-content`, but its `<main id="main-content">` has no `tabindex`. In browser verification on the Media Gallery page, the first Tab focused the skip link; activating it updated the fragment but left `document.activeElement` as `BODY`, not the main landmark.
- **Recommendation:** Add `tabindex="-1"` to each main landmark so fragment navigation can move keyboard focus to the destination. Verify that activating the skip link places focus on `main` and that subsequent Tab navigation starts within the main content.
- **Resolution:** Added `tabindex="-1"` to all three main landmarks and a scroll offset for the sticky navigation. Browser verification on each page confirmed activating the skip link moves focus to `main#main-content`.

No other actionable accessibility findings were identified in the reviewed scope.

## Verified positives

- Each page has one main landmark, a single page-level `h1`, and subsequent content headings at `h2`. The hero section is labelled by its page title.
- The desktop and mobile navigation provide the same five destinations, use the “Main navigation” label, and mark the current page with `aria-current="page"`. The mobile control uses native `<details>/<summary>` semantics.
- The skip link is first in document order and becomes visible on keyboard focus. Shared theme styles provide visible focus treatments for links and buttons; navigation controls have a gold focus outline.
- Calculated contrast ratios for the shared theme’s principal solid color pairs are: ink/paper **16.86:1**, muted/paper **7.33:1**, gold-dark/paper **4.78:1**, gold/night **12.72:1**, white/red **7.38:1**, ink/white **17.76:1**, and white/night **19.03:1**. These cover the corresponding solid token pairings, not every pixel of decorative gradients.
- The shared reduced-motion rule disables smooth scrolling, reduces transition duration, and removes the shared button hover translation. The secondary-page stylesheet adds no other animated movement.
- Phone and email actions use `tel:` and `mailto:` links with descriptive accessible names. Unverified social profiles remain plain text rather than misleading links.
- Gallery, video, and review content have clear pending-state text; no empty interactive player is presented.
- Parent browser verification reports no horizontal overflow at 320, 390, 768, 800, 960, or 1280 px; one main landmark per page; the first Tab landing on the skip link; and all five mobile navigation links appearing.

## Limitations

- Parent-provided viewport checks establish no horizontal overflow at the listed widths; they do not establish behavior at 200%/400% zoom or with enlarged text.
- No screen-reader/assistive-technology session was run. Future media embeds, supplied review images, image alternatives, third-party provider controls, and actual caption tracks cannot be verified until those assets are added.
- Contrast figures above are calculated for the listed solid token pairs only; gradient and translucent-overlay pixels were not individually measured.
