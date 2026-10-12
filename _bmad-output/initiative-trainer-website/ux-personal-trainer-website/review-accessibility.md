# Accessibility Review

**Scope:** Contract-level review of [DESIGN.md](DESIGN.md), [EXPERIENCE.md](EXPERIENCE.md), [.memlog.md](.memlog.md), and the referenced [product spec](../spec-personal-trainer-website/spec-personal-trainer-website.md), [pages and content](../spec-personal-trainer-website/pages-and-content.md), [implementation stack](../spec-personal-trainer-website/implementation-stack.md), and [one-month packages](../spec-personal-trainer-website/one-month-packages.md). No implemented site or review screenshots were available for runtime verification.

**Summary:** The contract has a solid accessibility floor and sensible release gates. Intended text-color combinations pass WCAG AA contrast calculations. The main gaps are untestable wording around reflow and interaction details, no defined equivalent for screenshot reviews or accessible-PDF checks, and unknown captions/privacy behavior for third-party videos. These are implementation risks, not confirmed failures in a built site.

**Severity count:** Critical 0 | High 0 | Moderate 5 | Low 2

## Documented Safeguards

- WCAG 2.2 AA is named; keyboard operation, visible focus, image alternatives, logical headings/landmarks/reading order, and zoom-readable package information are promised.
- Contact actions must use real destinations; missing details remain placeholders in data, not live broken links. The revised agreement is withheld until its obsolete booking-app clause is removed.
- Package details are not hidden behind interaction; narrow layouts should stack comparisons. Trainer identity and contact/location details are selectable text rather than image-only content.
- Review screenshots require source and reuse permission. The logo is not a substitute for trainer name, service area, or phone text.
- Contrast ratios calculated from the listed tokens: white/red 7.38:1; light-gold/dark 12.72:1; white/dark 19.03:1; secondary/base 7.33:1 (secondary/white 7.71:1); dark-gold/base 4.78:1; primary-ink/base 16.86:1. These pass normal-text AA for the specified pairings.

## Findings

### Moderate

1. **Reflow and text resize need measurable acceptance checks.** Mobile-first layout, stacked package comparison, fixed type sizes, and zoom-readable content are documented, but no minimum viewport or zoom checks are stated. Verify no loss or two-dimensional scrolling at 320 CSS px (including a 1280 px viewport at 400% zoom), and that text can be enlarged to 200% without clipping or loss of content/functionality. Fixed font sizes alone are not a defect; the rendered layout is what needs checking.

2. **Navigation, focus, and target details are promises rather than an implementation pattern.** Navigation behavior is intentionally deferred. Once chosen, preserve keyboard access and visible, unobscured focus; provide a way past repeated navigation, meaningful page titles and landmarks, and a logical DOM order. The 48 px action heights are a useful safeguard, but widths and other links/icon controls are unspecified; verify WCAG 2.2 minimum target size or its spacing exception. Do not infer a menu design from this review.

3. **Image alternatives need content-specific decisions.** The logo contains stylized “Regal Power Fitness” lettering; give it an appropriate concise alternative when it conveys identity, or an empty alternative when adjacent text already supplies that identity. “Useful alternative text” for review screenshots is required, but the actual screenshots are not present and the contract does not say how their review text, rating, and attribution remain available to assistive technology. Ensure an equivalent is available in the page’s reading flow rather than relying on a generic image label.

4. **Video accessibility beyond iframe titles and controls is unresolved.** Descriptive embed titles and operable provider controls are documented. Video URLs/content are not supplied, and captions for prerecorded speech or equivalent access to meaningful audio is not addressed; verify the actual embeds. Immediate loading is an explicit decision, so confirm provider controls remain keyboard-operable without changing that decision by assumption.

5. **The agreement gate does not establish PDF accessibility.** Withholding the obsolete PDF is a strong safeguard, and the contract makes the revised file a download/print resource. Before publishing it, verify that the supplied PDF has selectable text, usable tags/reading order, and accessible form or signature content if present. The current PDF was not assessed here.

### Low

1. **Do not use low-contrast tokens for essential boundaries or text.** Bright gold on the base surface and the subtle divider against base both calculate to 1.42:1. The design explicitly reserves bright gold for dark surfaces and uses the divider as separation; retain those limits. If a divider, border, or other graphic is needed to identify a control or state, check the applicable non-text contrast rather than treating the current token as sufficient.

2. **Immediate third-party embeds have a privacy consequence not resolved by the contract.** Loading YouTube/Instagram embeds as soon as the gallery loads can contact those providers before a visitor interacts. The spec lists privacy information for embedded media as an open question. This is a disclosure/implementation consideration, not a WCAG failure or a requirement here to add consent or defer loading.
