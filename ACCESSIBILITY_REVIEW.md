# Accessibility Review

## Scope
- Reviewed layout and style customizations in this repository.
- Focus areas: keyboard navigation, screen reader semantics, and color/visual usability.
- No website content text was changed.

## Findings
- **Keyboard focus visibility**: Interactive elements did not have a clear custom `:focus-visible` treatment, which can make keyboard navigation harder to track.
- **Landmark semantics for section listing**: The posts container in `layouts/section/list.html` used a generic `div`, which is less descriptive for assistive technologies.
- **Color contrast risk areas**: The palette uses low-contrast muted tones in some decorative UI areas. Body text contrast appears acceptable, but muted/decorative tones should continue to be monitored if reused for important text.

## Changes Made
- Added a clear `:focus-visible` style for links, buttons, and common form controls in `static/css/typography.css`.
  - Uses a visible outline and underline to improve keyboard focus tracking.
- Updated the section listing wrapper from `div` to `section` and connected it to the page heading with `aria-labelledby` in `layouts/section/list.html`.

## Validation
- Ran Hugo build successfully after changes.
- Performed manual visual verification and captured a screenshot of the updated UI.
