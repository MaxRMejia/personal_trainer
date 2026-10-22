# Accessibility Review

Scope: Services & Classes mockup and shared `site-navigation.css` / `site-theme.css`. Findings only.

## Findings

1. **Provide a keyboard bypass for repeated navigation.** The page begins with the shared header/navigation and then enters `<main>` without a skip link (`mockups/key-services-classes.html:513-538`). Add a focus-visible “Skip to main content” link before the header and a matching `id` on `<main>` so keyboard users can bypass the repeated links.

2. **Remove hover movement when reduced motion is requested.** The reduced-motion rule only shortens transitions (`mockups/site-theme.css:73-76`); button and package-card hover states still translate (`mockups/site-theme.css:71`; `mockups/key-services-classes.html:134-135`), causing an abrupt jump rather than eliminating movement. Override those transforms under `prefers-reduced-motion: reduce`, retaining a non-motion hover cue.
