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
updated: 2026-10-11
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
    fontFamily: 'Libre Baskerville'
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.2'
  display-mobile:
    fontFamily: 'Libre Baskerville'
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  body:
    fontFamily: 'Source Sans 3'
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
rounded:
  sm: 4px
  md: 6px
  lg: 8px
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
    rounded: '{rounded.md}'
    height: 48px
  contact-action:
    backgroundColor: '{colors.primary}'
    textColor: '{colors.primary-foreground}'
    rounded: '{rounded.md}'
    height: 48px
  agreement-download:
    backgroundColor: '{colors.surface-raised}'
    textColor: '{colors.ink-primary}'
    rounded: '{rounded.md}'
    height: 48px
  package-comparison:
    backgroundColor: '{colors.surface-raised}'
    textColor: '{colors.ink-primary}'
    rounded: '{rounded.sm}'
  video-embed:
    size: '16:9'
  review-image:
    size: '100%'
  brand-logo:
    size: 'contain'
  site-navigation: {}
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

Use Libre Baskerville for headings and Source Sans 3 for body text. The font families are user-approved; the listed sizes are provisional desktop/mobile defaults and use fixed values rather than viewport scaling. Keep body copy comfortable for reading package terms and contact details.

## Layout & Spacing

Use a mobile-first single-column reading flow, expanding into restrained desktop columns only where content comparison benefits. Keep sections unframed and full-width rather than stacking cards. Apply the 4/8/12/16/24/32 px spacing scale. Navigation placement and interaction style remain open for user input.

## Elevation & Depth

Prefer contrast between light surfaces and dark bands over shadows. Use borders only to distinguish tables or package comparisons; avoid decorative elevation.

## Shapes

Use restrained corners: 4 px small, 6 px medium, and 8 px maximum. Keep package and service information in clear rows or open sections, not nested cards.

## Components

- **page-surface** — base light reading surface with primary ink.
- **brand-band** — dark brand band with contrast-safe light gold accents.
- **brand-band-copy** — white text for body copy on dark bands.
- **secondary-copy** — secondary text for metadata and supporting details.
- **brand-accent-text** — dark gold emphasis on light surfaces.
- **divider** — subtle one-pixel separation between related rows.
- **home-classes-packages-action** — primary red action with white text, sized for touch; see [Home/About mockup](mockups/key-home-about.html).
- **contact-action** — high-contrast direct-contact action; render only when a real destination is configured; see [Contact/Location mockup](mockups/key-contact-location.html).
- **agreement-download** — outlined/light secondary action for downloading the revised agreement; see [Services & Classes mockup](mockups/key-services-classes.html).
- **package-comparison** — use readable rows or a narrow-screen stacked comparison for price, schedule, allowance, and terms; see [Services & Classes mockup](mockups/key-services-classes.html).
- **video-embed** — preserve a 16:9 viewing area and do not crop the provider player; see [Media Gallery mockup](mockups/key-media-gallery.html).
- **review-image** — show the complete supplied screenshot; do not crop text from a review; see [Reviews mockup](mockups/key-reviews.html).
- **brand-logo** — use the [imported Regal Power Fitness logo](imports/regal_logo.jpeg); do not rely on it to communicate trainer name, service area, or phone; see [Home/About mockup](mockups/key-home-about.html).
- **site-navigation** — make all required pages reachable; visual placement and interaction remain undecided pending user direction.

## Do's and Don'ts

| Do | Don't |
| --- | --- |
| Keep schedules, prices, contact details, and agreement terms easy to scan. | Put essential contact or local-search text inside an image. |
| Let the supplied logo carry the decorative brand detail. | Add unrelated ornamental fitness graphics or card-heavy page sections. |
| Use the logo alt text only when the adjacent text does not already name the brand. | Repeat identical logo text to screen readers when visible adjacent text already names the brand. |