# GitHub Header Link Design

## Goal

Add a clearly recognizable GitHub link to the upper-right corner of the academic profile page so visitors can quickly open `https://github.com/rrrrrzy`.

## Placement and Layout

- Replace the standalone language-toggle positioning wrapper with a compact upper-right utility group.
- Place the GitHub icon immediately to the left of the existing language button.
- Preserve the current centered header content and navigation.
- At viewport widths up to 768 px, move the utility group into normal document flow and center it above the header, matching the current mobile behavior of the language control.

## Visual Treatment

- Use the page's existing neutral border and text colors so the control feels native to the current restrained academic design.
- Render the GitHub mark as an inline SVG using `currentColor`; no external icon library or network request is required.
- Give the link a compact bordered control shape, visually consistent with the language button.
- Provide matching hover and keyboard-focus feedback for the GitHub link and language button.

## Link Behavior and Accessibility

- Link to `https://github.com/rrrrrzy`.
- Open the profile in a new tab with `target="_blank"`.
- Include `rel="noopener noreferrer"`.
- Add bilingual `aria-label` and `title` values that are updated by the existing language toggle.
- Mark the SVG as decorative so assistive technology announces only the link label.

## Scope

The change is limited to `index.html`: HTML, embedded CSS, and the existing language-toggle function. No external dependencies, analytics, or unrelated layout refactoring will be introduced.

## Verification

- Confirm the GitHub link has the correct URL, new-tab behavior, security attributes, and accessible label.
- Confirm the inline SVG is present and decorative.
- Confirm the language switch updates the GitHub link's bilingual accessible text.
- Confirm utility-group layout rules exist for both desktop and mobile breakpoints.
- Run an HTML parse/validation check and the repository's available tests, if any.
