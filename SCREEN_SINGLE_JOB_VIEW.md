# Screen 2: Single Job View / Candidate Pipeline (Kanban Board)

This document describes the design for the Single Job View, focusing on the candidate pipeline (Kanban board). It maintains consistency with `SCREEN_MAIN_DASHBOARD.md` for elements like the Top Navigation Bar and references `STYLE_GUIDE.md` for visual styling.

## 1. Overall Layout

*   **Persistent Top Navigation Bar:** The same Top Navigation Bar as described in `SCREEN_MAIN_DASHBOARD.md` will be present at the top.
    *   Styling: Refer to `SCREEN_MAIN_DASHBOARD.md` and `STYLE_GUIDE.md`.
    *   Active Link: The "Jobs" link in the top navigation bar might be styled as active if the user navigated from there.
*   **Main Content Area:** Below the Top Navigation Bar, this area will be dedicated to the specific job's details and its candidate pipeline, primarily featuring the Kanban board. The background will be `Background Light` (`#FFFFFF`) or `Background Medium` (`#F8F9FA`) for the overall content area.

---

## 2. Header Section (Below Top Navigation Bar)

This section provides context for the job being viewed and allows for high-level actions related to it. It will be positioned directly below the Top Navigation Bar and above the Kanban board.

*   **Job Title:**
    *   Content: Prominently displayed job title (e.g., "Senior Backend Engineer").
    *   Styling: `H1` (`2.25rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Position: Aligned to the left.

*   **Job Status Toggle:**
    *   Options: "Active," "Paused," "Closed."
    *   Appearance: A segmented control or a set of styled tabs is preferred for quick visual assessment and interaction.
        *   If Segmented Control:
            *   Container: Rounded rectangle with internal dividers.
            *   Selected Option: Background `Primary Accent` (`#007BFF`), Text `White` (`#FFFFFF`).
            *   Unselected Options: Background `Background Medium` (`#F8F9FA`) or `Background Light` (`#FFFFFF`) with `Text Primary` (`#212529`) or `Text Secondary` (`#6C757D`). Border `1px solid Background Dark` (`#E9ECEF`).
        *   If Tabs:
            *   Active Tab: `Text Primary` (`#212529`) or `Primary Accent` (`#007BFF`) with a bottom border in `Primary Accent`.
            *   Inactive Tabs: `Text Secondary` (`#6C757D`).
    *   Typography: `Body Text` (`1rem`, `400 Regular` or `500 Medium`) for labels.
    *   Position: To the right of the Job Title or below it on narrower screens. Ensures current status is immediately clear.

*   **"Edit Job" Button:**
    *   Text: "Edit Job"
    *   Styling: Uses **Secondary Button** style from `STYLE_GUIDE.md`.
        *   Background Color: `#FFFFFF` (White) or `transparent`.
        *   Text Color: `Primary Accent` (`#007BFF`).
        *   Border: `1px solid` `Primary Accent` (`#007BFF`).
        *   Padding: `0.5rem 1rem` (consistent with nav bar secondary actions if space is tight, or standard `0.75rem 1.5rem`).
        *   Corner Radius: `0.375rem` (6px).
    *   Position: Typically aligned to the far right of this header section, or adjacent to the Job Status Toggle.

---

## 3. Kanban Board View

The Kanban board is the primary interface for managing candidates through the hiring pipeline. It should be visually clean, intuitive to use, and provide clear information at a glance.

*   **General Structure:**
    *   A horizontally scrollable area if the number of columns exceeds the viewport width.
    *   Columns represent the different stages of the hiring process.
    *   Consistent spacing between columns to avoid a cramped look.

*   **Column Styling:**
    *   **Header (per column):**
        *   Titles: "Applied," "Shortlisted," "Interviewing," "Offer," "Hired." Additional custom stages might be possible in a future iteration, but these are the defaults.
        *   Styling: `H4` (`1.125rem`, `600 Semi-Bold`) from `STYLE_GUIDE.md`.
        *   Color: `Text Primary` (`#212529`) or `Text Secondary` (`#6C757D`).
        *   Candidate Count: Displayed next to the title or below it, e.g., "Applied (12)".
            *   Styling: `Small Text` (`0.875rem`, `400 Regular`) with `Text Secondary` (`#6C757D`).
        *   Padding: `0.75rem 1rem` for the header area within each column.
        *   Border: A subtle bottom border using `Background Dark` (`#E9ECEF`) to separate the header from the candidate cards within the column.
    *   **Column Body:**
        *   Background: `Background Medium` (`#F8F9FA`) or a very light tint of `Primary Accent` to subtly differentiate from the main page background (`#FFFFFF`).
        *   Padding: `1rem` around the area where cards are placed.
        *   Corner Radius: `0.375rem` (6px) for the overall column.
        *   Min-Height: Ensure columns have a minimum height even when empty to maintain layout consistency and provide a clear drop zone.
    *   **Spacing:** `1rem` margin between columns.

*   **Candidate Cards (Draggable):**
    *   **Layout & Styling:**
        *   Shape: Rectangular cards.
        *   Background: `Background Light` (`#FFFFFF`).
        *   Border: `1px solid Background Dark` (`#E9ECEF`).
        *   Shadow: Subtle box shadow (e.g., `0 1px 3px rgba(0,0,0,0.1)`) for a "lifted" effect, making them feel draggable.
        *   Padding: `0.75rem` to `1rem` internal padding.
        *   Corner Radius: `0.375rem` (6px).
        *   Margin: `0.75rem` bottom margin between cards within a column.
    *   **Content on Card:**
        *   **Candidate Name:**
            *   Styling: `H4` (`1.125rem`, `600 Semi-Bold`) or bold `Body Text` (`1rem`, `700 Bold`).
            *   Color: `Text Primary` (`#212529`).
        *   **Photo/Avatar:**
            *   Size: `32px` or `40px` diameter, circular.
            *   Position: Top-left of the card, or to the left of the name.
            *   Placeholder: Initials or a generic icon if no image is available, with `Background Medium` (`#F8F9FA`).
        *   **Headline/Last Role:** (e.g., "Senior Software Engineer at Tech Solutions Inc.")
            *   Styling: `Small Text` (`0.875rem`, `400 Regular`).
            *   Color: `Text Secondary` (`#6C757D`).
            *   Position: Below the candidate name.
        *   **Icons (Small & Subtle):** Arranged horizontally, typically at the bottom of the card or below the headline.
            *   **Resume Icon:** Standard document icon.
                *   Action: On click, triggers resume download or opens in a new tab/modal (details in Screen 3).
                *   Color: `Text Secondary` (`#6C757D`). Hover: `Primary Accent` (`#007BFF`).
            *   **Public Profile Link Icon:** Standard external link icon or LinkedIn icon.
                *   Action: On click, opens profile link in a new browser tab.
                *   Color: `Text Secondary` (`#6C757D`). Hover: `Primary Accent` (`#007BFF`).
            *   These icons should have appropriate tooltips on hover.
        *   **New Feedback Indicator:**
            *   Appearance: A small, filled circle (dot).
            *   Color: `Information` color (`#17A2B8`) or `Primary Accent` (`#007BFF`).
            *   Position: Top-right corner of the card, or next to the candidate's name.
            *   Tooltip: On hover, "New feedback available."
    *   **Interactive States for Candidate Card:**
        *   **Default:** As styled above.
        *   **Hover:**
            *   Shadow: Slightly more pronounced shadow (e.g., `0 2px 6px rgba(0,0,0,0.15)`).
            *   Border: Border color might change to `Primary Accent Hover` (`#0056b3`).
        *   **Selected/Clicked (for viewing details, before dragging):**
            *   Border: `2px solid Primary Accent` (`#007BFF`).
            *   Background: No change or a very slight tint like `#E6F2FF` (a lighter shade of blue).
        *   **Dragging:**
            *   Opacity: Reduced to `0.8` or `0.85`.
            *   Rotation: Optionally, a very slight tilt (e.g., 2-3 degrees) to enhance the "picked up" feel.
            *   Drop Zone Indication: When hovering over a valid column, the column might show a placeholder (dashed border rectangle) or the existing cards shift to indicate the drop position.

---

## 4. Rejected Candidates Area

To maintain a clean Kanban board focused on active candidates while ensuring rejected candidates are still accessible for review or potential reconsideration, a dedicated area is required.

*   **Accessibility & Implementation Idea:**
    *   A "View Rejected Candidates" link/button will be provided. This is preferred over a collapsible section at the bottom for a cleaner initial view of the active pipeline.
    *   **Position:** This link/button could be placed near the Kanban board's title area (e.g., alongside the "Active Jobs" title on the main dashboard, or near the Job Status Toggle in this view) or as a distinct, visually separated "column" at the end of the Kanban board that doesn't contain draggable cards but acts as an entry point.
    *   For this design, let's place a button in the Header Section, near the "Edit Job" button, or as a tab-like element next to a "Kanban View" tab.
    *   Alternative: The last column of the Kanban board could be titled "Rejected" and styled differently (e.g., grayed out slightly). Clicking on this column/header could then lead to a separate list view or modal. However, for better separation, a dedicated button/link is cleaner.

*   **"View Rejected Candidates" Link/Button:**
    *   Text: "View Rejected Candidates" or simply "Rejected (X)" where X is the count.
    *   Styling:
        *   If **Link Button Style**: `Primary Accent` (`#007BFF`) text, underline on hover. Appropriate for a less prominent action.
        *   If **Secondary Button Style**: `Background Light` (`#FFFFFF`), `Text Primary Accent` (`#007BFF`), border `1px solid Primary Accent` (`#007BFF`). Suitable if more visual weight is desired.
        *   Let's choose **Link Button** style for a less cluttered header.
    *   Position: In the Header Section (Section 2), to the right, perhaps grouped with the "Edit Job" button or below the Job Status Toggle.

*   **Interaction:**
    *   Clicking the "View Rejected Candidates" link/button will:
        *   Open a modal dialog displaying a list of rejected candidates for the current job.
        *   OR, navigate to a separate tabbed view on this page that lists rejected candidates.
    *   The list should include: Candidate Name, Date of Rejection, Reason for Rejection (if available), and a link to their full profile/application details.
    *   This list should be searchable and sortable.

---
