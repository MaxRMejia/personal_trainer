# UX Rubric Review — Services & Classes

## Actionable findings

1. **Tablet contact actions become unwieldy.** In `ux-personal-trainer-website/mockups/key-services-classes.html:433-441`, the 761–960 px media query is nested inside the `max-width: 760px` query, so it cannot apply. At 800 px, the package cards remain side by side and their contact buttons render about 139 × 105 px, wrapping the labels into tall controls (`:204-214`). Move the tablet rule outside the mobile query or correct the breakpoint, then verify the package actions at tablet widths.

2. **Out-of-scope source note not adopted.** The user explicitly limited this pass to the existing Services mockup copy and excluded the broader requirements document. No content suggestions from that excluded source were used or added.
