# Nexus HR Portal: Key Interactive States

This document describes common key interactive states for UI elements across the Nexus HR Portal. It complements `STYLE_GUIDE.md` and the individual screen designs (Screens 1-4) to ensure a consistent and predictable user experience.

## 1. General Principles

*   **Clear Visual Feedback:** User interactions must always result in clear and immediate visual feedback. This helps users understand the system's response and their own actions.
*   **Consistency:** All interactive states should be consistent with the defined `STYLE_GUIDE.md` (colors, typography, spacing) and applied uniformly across the portal.
*   **Accessibility:** States, especially focus states, must meet accessibility standards (WCAG AA) to ensure usability for everyone, including keyboard-only users and those using assistive technologies.

---

## 2. Buttons (General Recap & Additions)

Referencing `STYLE_GUIDE.md` for base styles.

*   **Primary Button (`Primary Accent` background, `White` text):**
    *   **Hover:** Slightly darker background (`Primary Accent Hover: #0056b3`).
    *   **Active/Pressed:** Even darker background (`Primary Accent Active: #004085`) or subtle inset shadow.
    *   **Disabled:** Lighter background (`#A0CFFF` or `Background Dark: #E9ECEF`), muted text (`Text Secondary` or `#BDC3C7`), `not-allowed` cursor.
*   **Secondary Button (White background, `Primary Accent` text & border):**
    *   **Hover:** Background `Primary Accent`, Text `White`.
    *   **Active/Pressed:** Background `Primary Accent Active`, Text `White`.
    *   **Disabled:** Lighter text & border (`#A0CFFF` or `#CED4DA`), `not-allowed` cursor. Background `Background Dark` or remains white.
*   **Link Button (`Primary Accent` text, transparent background):**
    *   **Hover:** Text color `Primary Accent Hover`, `underline`.
    *   **Active/Pressed:** Text color `Primary Accent Active`, `underline`.
    *   **Disabled:** Muted text color (`#A0CFFF` or `#BDC3C7`), no underline, `not-allowed` cursor.
*   **Focus State (Keyboard Navigation - Applies to all button types):**
    *   A distinct outline will appear around the button.
    *   Style: `2px solid Primary Accent` (`#007BFF`) or `Primary Accent Hover` (`#0056b3`) offset slightly from the button edge (using `outline` and `outline-offset`). This ensures visibility on different background colors.

---

## 3. Input Fields (Text, Textarea, Select Dropdowns)

Referencing general input styling from `SCREEN_CREATE_JOB_FORM.md` and `STYLE_GUIDE.md`.

*   **Default State:**
    *   Border: `1px solid Background Dark` (`#E9ECEF`).
    *   Background: `Background Light` (`#FFFFFF`).
    *   Text Color: `Text Primary` (`#212529`).
*   **Hover State:**
    *   Border: `1px solid Text Secondary` (`#6C757D`) or a light shade of `Primary Accent`. (Subtle change to indicate interactivity).
*   **Focus State:**
    *   Border: `1px solid Primary Accent` (`#007BFF`).
    *   Box Shadow: Optional subtle shadow in `Primary Accent` (e.g., `0 0 0 2px rgba(0, 123, 255, 0.25)`).
*   **Filled/Valid State (Optional, if aggressive inline validation is used):**
    *   Standard appearance after valid input.
    *   Optional: A small green checkmark icon (`Success/Positive` color) inside the field on the right.
*   **Error State:**
    *   Border: `1px solid Danger/Alerts` (`#DC3545`).
    *   Icon (Optional): Small warning triangle icon (`Danger/Alerts` color) inside or next to the field.
    *   Helper Text: Error message displayed below the field using `Danger/Alerts` color and `Small Text` typography.
*   **Disabled State:**
    *   Background: `Background Dark` (`#E9ECEF`) or a very light gray.
    *   Border: `1px solid Background Dark` (`#E9ECEF`) or a lighter gray.
    *   Text Color: `Text Secondary` (`#6C757D`) or muted.
    *   Cursor: `not-allowed`.

---

## 4. Kanban Cards (Recap & Expansion from Screen 2)

Referencing `SCREEN_SINGLE_JOB_VIEW.md` for base styles.

*   **Default State:**
    *   Background: `Background Light` (`#FFFFFF`).
    *   Border: `1px solid Background Dark` (`#E9ECEF`).
    *   Shadow: Subtle box shadow (e.g., `0 1px 3px rgba(0,0,0,0.1)`).
*   **Hover State:**
    *   Shadow: Slightly more pronounced (e.g., `0 2px 6px rgba(0,0,0,0.15)`).
    *   Border: Color may change to `Primary Accent Hover` (`#0056b3`) or a slightly darker gray.
*   **Selected/Active (e.g., when clicked to open Candidate Profile - Screen 3):**
    *   Border: `2px solid Primary Accent` (`#007BFF`).
    *   Background: Optional very slight tint like `#E6F2FF` (a lighter shade of blue).
*   **Dragging State:**
    *   Opacity: Reduced (e.g., `0.8` to `0.9`).
    *   Shadow: May increase slightly to enhance the "lifted" perception.
    *   Rotation (Optional): Very slight tilt (e.g., 2-3 degrees).
*   **Drop Target Indication (Kanban Columns):**
    *   When dragging a card over a valid column:
        *   Column Background: May lighten or receive a tint of `Primary Accent`.
        *   Placeholder: A dashed outline placeholder may appear within the column indicating where the card would drop.
        *   Existing cards in the column may shift to visually make space.

---

## 5. Navigation Links (Top Bar, Tabs, Breadcrumbs)

*   **Default State:**
    *   Top Bar Links: `Primary Accent` (`#007BFF`) as per `STYLE_GUIDE.md` Link Button style.
    *   Tab Links (Inactive): `Text Secondary` (`#6C757D`) or `Text Primary` (`#212529`).
    *   Breadcrumb Links: `Text Secondary` (`#6C757D`), with the current page (non-link) `Text Primary`.
*   **Hover State:**
    *   Top Bar Links: Text color `Primary Accent Hover` (`#0056b3`), `underline`.
    *   Tab Links: Text color `Primary Accent` (`#007BFF`) or `Text Primary` if already dark, possible subtle underline or background change (`Background Medium`).
    *   Breadcrumb Links: Underline and color change to `Primary Accent`.
*   **Active/Current Page State:**
    *   Top Bar Links: `Text Primary` (`#212529`) or a bolder version of `Primary Accent`, often with a subtle underline or bottom border in `Primary Accent`.
    *   Tabs: `Text Primary` (`#212529`) or `Primary Accent`, with a prominent bottom border in `Primary Accent`. Font weight might be bolder (`600 Semi-Bold`).
    *   Breadcrumbs: Current page is non-interactive, styled as `Text Primary` and often bolder.
*   **Focus State (Keyboard Navigation - Applies to all link types):**
    *   Similar to buttons: A visible outline (`2px solid Primary Accent` or `Primary Accent Hover`) offset slightly. For links within text blocks, the default browser focus outline might be acceptable if sufficiently visible.

---

## 6. Dropdown Menus (e.g., User Profile Dropdown, Select Dropdowns)

*   **Trigger Element (Button or Field that opens the dropdown):**
    *   **Default:** Styled as a button (e.g., User Profile in Nav Bar) or an input field (Selects).
    *   **Hover:** Subtle background change or border highlight on the trigger element. For select fields, this follows input hover.
    *   **Active/Open:** State of the trigger might change (e.g., arrow icon pointing up instead of down). Trigger remains highlighted while dropdown is open.
*   **Dropdown Panel (Once Open):**
    *   Background: `Background Light` (`#FFFFFF`).
    *   Border: `1px solid Background Dark` (`#E9ECEF`) or `Text Secondary`.
    *   Shadow: Subtle dropdown shadow (e.g., `0 2px 5px rgba(0,0,0,0.15)`).
    *   Corner Radius: `0.25rem` or `0.375rem`.
*   **Item Hover (within the dropdown list):**
    *   Background: `Background Medium` (`#F8F9FA`) or a light tint of `Primary Accent` (e.g., `#E6F2FF`).
    *   Text Color: May change to `Primary Accent` or remain `Text Primary` for contrast.
*   **Selected Item (in a custom select dropdown, not the main user profile dropdown):**
    *   Indication: A checkmark icon next to the selected item's text.
    *   Font Weight: May become bolder (`600 Semi-Bold`).
    *   Background: Could have a slightly different persistent background if the dropdown remains open.
*   **Focus State (Keyboard Navigation):**
    *   Trigger: Standard focus outline.
    *   Items within Dropdown: As items are navigated via keyboard, they should display the same style as "Item Hover."

---

## 7. Notifications & Alerts

*   **Notification Bell Icon (Top Navigation Bar - Recap from Screen 1):**
    *   Default: `Text Secondary` (`#6C757D`).
    *   With Unread Items: Icon color changes to `Primary Accent` (`#007BFF`). A small red (`Danger/Alerts`) badge appears on the top-right of the icon, possibly with a count.
*   **Toast Notifications (for actions like "Job Published," "Draft Saved," "Error Occurred"):**
    *   Appearance: Rectangular boxes, typically appearing in a corner of the screen (e.g., top-right or bottom-center).
    *   Layout: Icon + Text. Max width to prevent overly wide toasts.
    *   Styling:
        *   Background:
            *   Success: `Success/Positive` (`#28A745`).
            *   Error: `Danger/Alerts` (`#DC3545`).
            *   Information: `Information` (`#17A2B8`) or `Background Medium` (`#F8F9FA`) with a colored left border.
            *   Warning: `Warning/In-Progress` (`#FFC107`).
        *   Text Color: `White` (`#FFFFFF`) for dark backgrounds (Success, Error, Warning), or `Text Primary` for light backgrounds.
        *   Icon: Appropriate icon for the status (checkmark, 'x', 'i', warning sign).
        *   Shadow: Subtle shadow.
        *   Corner Radius: `0.25rem` or `0.375rem`.
    *   Interaction:
        *   Auto-dismiss: Typically disappear after 3-5 seconds.
        *   Close Button ('x'): Allows manual dismissal. Styled subtly. Hover state on close button should be visible.

---

## 8. Modals/Dialogs (e.g., "Use Template" Modal, "Reject Candidate" Confirmation)

*   **Overlay:**
    *   Color: Semi-transparent black (e.g., `rgba(0, 0, 0, 0.5)` or `rgba(33, 37, 41, 0.6)` using `Text Primary` at partial opacity).
    *   Action: Clicking the overlay usually closes the modal (unless it's a critical confirmation).
*   **Modal Container:**
    *   Background: `Background Light` (`#FFFFFF`).
    *   Border: Optional, `1px solid Background Dark` (`#E9ECEF`).
    *   Shadow: Prominent shadow to lift it above the overlay (e.g., `0 4px 15px rgba(0,0,0,0.2)`).
    *   Corner Radius: `0.375rem` to `0.5rem`.
    *   Padding: Generous internal padding (e.g., `1.5rem` to `2rem`).
*   **Header (within Modal):**
    *   Background: Optional, `Background Medium` (`#F8F9FA`) or same as modal.
    *   Title: `H3` or `H4` styling.
    *   Close Button ('x'): Positioned top-right of the modal or modal header.
        *   Styling: Icon button, `Text Secondary` color, changes to `Text Primary` or `Danger/Alerts` on hover for visual feedback.
*   **Focus Management:**
    *   Focus should be programmatically trapped within the modal when it opens.
    *   The first interactive element (e.g., an input field or a button) or the close button should receive initial focus.
    *   Escape key press should close the modal.
*   **Buttons within Modal (e.g., "Confirm," "Cancel"):**
    *   Styled according to `Primary Button`, `Secondary Button` definitions.
    *   Typically aligned to the right of the modal footer.

---

## 9. Tooltips

*   **Trigger:** On hover (or focus for keyboard users) over an element (e.g., icon, truncated text, disabled button) that requires additional explanation.
*   **Appearance:**
    *   Shape: Small, rectangular box with slightly rounded corners (`0.25rem`).
    *   Background: `Text Primary` (`#212529`) or a dark gray.
    *   Text Color: `White` (`#FFFFFF`) or a light gray.
    *   Typography: `Small Text` (`0.875rem`).
    *   Padding: `0.25rem 0.5rem`.
    *   Pointer (Optional): Small triangle pointing towards the trigger element.
*   **Behavior:**
    *   Delay: Appears after a brief delay (e.g., 300-500ms) to avoid appearing on accidental mouse-overs.
    *   Positioning: Appears near the trigger element (above, below, left, or right, depending on available space), without obscuring critical information.
    *   Disappears: When the mouse moves away from the trigger or focus is lost.

---
