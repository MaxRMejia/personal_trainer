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
updated: 2026-10-21
colors:
  surface-base: '#FAF9F6'
  surface-raised: '#FFFFFF'
  surface-dark: '#101010'
  ink-primary: '#181818'
  ink-secondary: '#57524E'
  border-subtle: '#D8D2CB'
  primary: '#B00000'
  primary-foreground: '#FFFFFF'
  brand-gold-dark: '#A06010'
  brand-gold-light: '#F0D080'
typography:
  display:
    fontFamily: 'Playfair Display'
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.08'
  display-mobile:
    fontFamily: 'Playfair Display'
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.08'
  body:
    fontFamily: 'DM Sans'
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.65'
rounded:
  sm: 12px
  md: 18px
  lg: 24px
  pill: 999px
spacing:
  '1': 4px
  '2': 8px
  '3': 12px
  '4': 16px
  '5': 24px
  '6': 32px
components:
  page-surface:
    backgroundColor: '{colors.surface-base}'
    textColor: '{colors.ink-primary}'
  brand-band:
    backgroundColor: '{colors.surface-dark}'
    textColor: '{colors.brand-gold-light}'
  brand-band-copy:
    backgroundColor: '{colors.surface-dark}'
    textColor: '{colors.primary-foreground}'
  secondary-copy:
    backgroundColor: '{colors.surface-base}'
    textColor: '{colors.ink-secondary}'
  brand-accent-text:
    backgroundColor: '{colors.surface-base}'
    textColor: '{colors.brand-gold-dark}'
  divider:
    backgroundColor: '{colors.border-subtle}'
    height: 1px
  home-classes-packages-action:
    backgroundColor: '{colors.primary}'
    textColor: '{colors.primary-foreground}'
    rounded: '{rounded.pill}'
    height: 52px
  contact-action:
    backgroundColor: '{colors.primary}'
    textColor: '{colors.primary-foreground}'
    rounded: '{rounded.pill}'
    height: 52px
  agreement-download:
    backgroundColor: '{colors.surface-raised}'
    textColor: '{colors.ink-primary}'
    rounded: '{rounded.pill}'
    height: 48px
  package-comparison:
    backgroundColor: '{colors.surface-raised}'
    textColor: '{colors.ink-primary}'
    rounded: '{rounded.lg}'
  video-embed:
    size: '16:9'
  review-image:
    size: '100%'
  brand-logo:
    size: 'contain'
    desktopSize: 80px
    mobileSize: 64px
    narrowMobileSize: 56px
  trainer-photo:
    size: 'cover'
    rounded: '{rounded.sm}'
  site-navigation:
    backgroundColor: 'rgba(16, 16, 16, 0.84)'
    textColor: '{colors.primary-foreground}'
    activeColor: '{colors.brand-gold-light}'
    minHeight: 82px
    rounded: '{rounded.sm}'
  page-intro:
    backgroundColor: '{colors.surface-dark}'
    textColor: '{colors.primary-foreground}'
    minHeight: 420px
    mobileMinHeight: 340px
---

## Brand & Style

Regal Power Fitness is an energetic personal-training brand anchored by its supplied crown-and-barbell logo. Use light reading surfaces for information and darker bands to carry the logo's dramatic black, red, and metallic-gold identity. Keep fitness information direct and confident; the logo supplies the ornament, so page chrome stays disciplined.

## Colors

- **Light surfaces (`{colors.surface-base}`, `{colors.surface-raised}`)** support long-form service, schedule, and agreement details.
- **Dark band (`{colors.surface-dark}`)** anchors brand moments and pairs with white text and light gold accents (`{colors.brand-gold-light}`).
- **Deep red (`{colors.primary}`)** is the primary action color; white text on it measures 7.38:1 contrast.
- **Dark gold (`{colors.brand-gold-dark}`)** may accent text on light surfaces; it measures 4.78:1 against the base surface. Bright gold (`{colors.brand-gold-light}`) is reserved for dark surfaces, where it measures 12.72:1.
- **Ink tokens** retain strong reading contrast: primary ink on the base is 16.86:1, secondary ink on the base is 7.33:1, and white on the dark band is 19.03:1.
- **Border (`{colors.border-subtle}`)** is a decorative divider only, at 1.42:1 against the base; never use it alone to identify a control, boundary, or state.

## Typography

Use Playfair Display for editorial headings and DM Sans for body and interface text, with Libre Baskerville/Georgia and Source Sans 3/Arial fallbacks. Load the selected fonts through Google Fonts. Scale headings responsively while keeping body copy at 16 px or larger for package terms and contact details.

## Layout & Spacing

Use a mobile-first single-column reading flow, expanding into restrained desktop columns where comparison benefits. Use the 4/8/12/16/24/32 px spacing scale and generous section spacing. All five mockups load the shared navigation from [site-navigation.css](mockups/site-navigation.css); its floating smoked-glass surface, blur, inset, logo sizing (80 px desktop, 64 px mobile, 56 px narrow mobile), active state, and mobile disclosure stay consistent with Home. The shared theme in [site-theme.css](mockups/site-theme.css) owns palette, typography, spacing, radii, and button foundations for the modernized Home and Services mockups. The Services hero is intentionally compact, while Home retains its image-led entry moment.

## Elevation & Depth

Use soft, low-opacity shadows to lift package cards and callouts; retain subtle borders for definition. Keep the palette contrast—not shadow—responsible for hierarchy.

## Shapes

Use 12 px for compact surfaces, 18 px for grouped policy items, 24 px for cards, and pill-shaped buttons. Do not nest cards.

## Components

- **page-surface** — base light reading surface with primary ink.
- **brand-band** — dark brand band with contrast-safe light gold accents.
- **brand-band-copy** — white text for body copy on dark bands.
- **secondary-copy** — secondary text for metadata and supporting details.
- **brand-accent-text** — dark gold emphasis on light surfaces.
- **divider** — subtle one-pixel separation between related rows.
- **home-classes-packages-action** — primary red action with white text, sized for touch; see [Home/About mockup](mockups/key-home-about.html).
- **contact-action** — high-contrast direct-contact action; render only when a real destination is configured; see [Contact/Location mockup](mockups/key-contact-location.html).
- **agreement-download** — show a disabled, non-interactive control while the revised agreement is pending; enable a static PDF download only when the approved file is ready.
- **package-comparison** — use two responsive cards for price, schedule, allowance, and contact actions; distinguish one with the dark brand surface. Keep all terms visible; see [Services & Classes mockup](mockups/key-services-classes.html).
- **policy-list** — split existing policies into readable, icon-led items; use a soft callout for the pending agreement and keep its unavailable download visibly disabled.
- **contact-band** — close Services with a dark brand band and prominent, palette-styled phone/email links.
- **video-embed** — preserve a 16:9 viewing area and do not crop the provider player; see [Media Gallery mockup](mockups/key-media-gallery.html).
- **review-image** — show the complete supplied screenshot; do not crop text from a review; see [Reviews mockup](mockups/key-reviews.html).
- **brand-logo** — use the [imported Regal Power Fitness logo](imports/regal_logo.jpeg); do not rely on it to communicate trainer name, service area, or phone; see [Home/About mockup](mockups/key-home-about.html).
- **trainer-photo** — use a trainer-approved original photo; preserve Lynette's real appearance, crop to keep the subject clear, and do not show another business's signage or apparel branding; see [Home/About mockup](mockups/key-home-about.html).
- **site-navigation** — use the shared [navigation stylesheet](mockups/site-navigation.css) and identical markup on all five mockups; use horizontal links on desktop and an expandable, keyboard-operable menu on mobile; highlight the current page in light gold. See [Home/About mockup](mockups/key-home-about.html).
- **page-intro** — keep secondary-page title bands generous and vertically aligned, with enough space to echo the Home hero without making content pages feel like another landing page; see the [Media Gallery mockup](mockups/key-media-gallery.html), [Reviews mockup](mockups/key-reviews.html), and [Contact/Location mockup](mockups/key-contact-location.html). Services uses its own compact branded hero.

## Do's and Don'ts

| Do | Don't |
| --- | --- |
| Keep schedules, prices, contact details, and agreement terms easy to scan. | Put essential contact or local-search text inside an image. |
| Let the supplied logo carry the decorative brand detail and use approved photography to add a personal connection. | Add unrelated ornamental fitness graphics, show another business's branding, or use cards outside focused package and policy groupings. |
| Use the logo alt text only when the adjacent text does not already name the brand. | Repeat identical logo text to screen readers when visible adjacent text already names the brand. |
| Reserve raised cards for package comparison and tightly related policy items. | Invent package features, benefits, badges, testimonials, discounts, or recurring-billing language. |