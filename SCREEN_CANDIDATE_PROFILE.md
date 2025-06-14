# Screen 3: Candidate Profile & Feedback Hub

This document outlines the design for the Candidate Profile & Feedback Hub. It maintains consistency with `SCREEN_MAIN_DASHBOARD.md` and `SCREEN_SINGLE_JOB_VIEW.md` for shared elements like the Top Navigation Bar, and references `STYLE_GUIDE.md` for all visual styling.

## 1. Overall Layout

*   **Persistent Top Navigation Bar:** The standard Top Navigation Bar as described in `SCREEN_MAIN_DASHBOARD.md` will be present.
    *   Styling: Refer to `SCREEN_MAIN_DASHBOARD.md` and `STYLE_GUIDE.md`.
*   **Main Content Area:** Below the Top Navigation Bar, the layout will be a clear two-column structure.
    *   **Left Column:** Dedicated to displaying comprehensive Candidate Information.
    *   **Right Column:** Serves as the Feedback & Action Hub.
    *   Background: The overall content area background will be `Background Light` (`#FFFFFF`).
    *   Spacing: Adequate spacing between the columns and surrounding elements to ensure an uncluttered view.

---

## 2. Header Section (Below Top Navigation Bar, specific to this screen)

This section provides context for the candidate profile being viewed and allows for easy navigation.

*   **Candidate Name (as Page Title):**
    *   Content: Full name of the candidate (e.g., "Anjali Sharma").
    *   Styling: `H1` (`2.25rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Position: Prominently at the top-left of the main content area.

*   **"Back to [Job Title] Pipeline" Link:**
    *   Text Example: "Back to Senior Backend Engineer Pipeline" or "‹ Back to Pipeline".
    *   Styling: **Link Button** style from `STYLE_GUIDE.md`.
        *   Text Color: `Primary Accent` (`#007BFF`).
        *   Hover State: Text Color `Primary Accent Hover` (`#0056b3`), `underline`.
        *   Font Size: `Small Text` (`0.875rem`) or `Body Text` (`1rem`).
        *   Icon: Optionally, a small left-pointing arrow icon (e.g., "‹") can precede the text.
    *   Position: Below the Candidate Name or to its right on wider screens. Enables easy navigation back to Screen 2 (Kanban View).

*   **Optional Key Action Buttons:**
    *   Consideration: For high visibility and efficient workflow, primary action buttons like "Move to Next Stage" or "Schedule Interview" (relevant to the candidate's current status) could be duplicated here from the Right Column's action hub.
    *   Styling: Use **Primary Button** or **Secondary Button** styles as appropriate, possibly slightly smaller versions if space is a concern.
    *   Position: Typically aligned to the right of this header section, opposite the Candidate Name.

---

## 3. Left Column: Candidate Information

This column provides a comprehensive overview of the candidate's profile, application, and history. It should be well-organized and easy to scan. The column will have a background of `Background Light` (`#FFFFFF`) or `Background Medium` (`#F8F9FA`) if a visual distinction for the entire column is desired.

### Candidate Identity Block:

*   **Layout:** Positioned at the top of the Left Column.
*   **Photo/Avatar:**
    *   Size: `80px` to `100px` diameter, circular.
    *   Placeholder: Initials or a generic profile icon on `Background Medium` (`#F8F9FA`) if no image.
*   **Name:**
    *   Styling: `H3` (`1.375rem`, `600 Semi-Bold`) or `H2` if the page title H1 is very large.
    *   Color: `Text Primary` (`#212529`).
    *   Position: To the right of or below the avatar.
*   **Contact Details:**
    *   Content: Email, Phone (if available).
    *   Styling: `Body Text` (`1rem`, `400 Regular`). Each item on a new line or clearly separated.
    *   Icons: Precede email with an envelope icon, phone with a phone icon. Icon color `Text Secondary` (`#6C757D`).
*   **Links (e.g., LinkedIn, Portfolio, GitHub):**
    *   Display: List of links with corresponding icons (e.g., LinkedIn icon, GitHub icon, generic link icon).
    *   Styling: Text styled as **Link Button** (`Primary Accent` text, underline on hover). `Body Text` size.
    *   Arrangement: Below contact details.

### Built-in PDF Viewer (Resume Display):

*   **Area Designation:** A clearly defined rectangular area below the Candidate Identity Block.
*   **Viewer:**
    *   Implementation: Embed a JavaScript-based PDF viewer (e.g., PDF.js or a similar library).
    *   Background: The viewer itself will likely have its own interface, but the container should blend with the column background.
    *   Height: Should occupy a significant portion of the Left Column, e.g., `400px` to `600px`, or be dynamically sized with a max-height and internal scrolling.
*   **Functionality:**
    *   Scrolling: Vertical scrolling within the PDF document is essential.
    *   Controls (Standard PDF Viewer Controls):
        *   Zoom In / Zoom Out.
        *   Download PDF button.
        *   Print PDF button.
        *   Page navigation (if multi-page resume).
    *   Fallback: If a full viewer is too complex for an initial version, display the first page as an image and provide a prominent "Download Full Resume" link styled as a **Primary Button** or **Secondary Button**. However, the brief specifies "built-in PDF viewer."
*   **Border:** A subtle border `1px solid Background Dark` (`#E9ECEF`) around the viewer area.

### Application Details:

*   **Position:** Below the PDF viewer or in a less prominent side section within this left column if space is tight.
*   **Content & Styling:**
    *   "**Applied for:** [Job Title]" - Job Title can be a link to Screen 2.
    *   "**Date Applied:** [Date]"
    *   "**Source:** [e.g., LinkedIn, Referral by John Doe, Careers Page]"
    *   Typography: Labels in `Small Text` (`0.875rem`, `600 Semi-Bold`) with `Text Secondary` (`#6C757D`), and values in `Small Text` (`0.875rem`, `400 Regular`) with `Text Primary` (`#212529`).
    *   Layout: Each item on a new line.

### Timeline/Activity Log:

*   **Title:** "Activity" or "Candidate Timeline."
    *   Styling: `H4` (`1.125rem`, `600 Semi-Bold`).
*   **Layout:** A chronological list of events, ordered from newest to oldest.
*   **Item Content Example:**
    *   "Oct 29, 2023 - Interview feedback received from Rohan Kumar."
    *   "Oct 27, 2023 - Moved to 'Shortlisted' stage by Priya Sharma."
    *   "Oct 26, 2023 - Applied for Senior Backend Engineer."
*   **Item Styling:**
    *   Typography: `Small Text` (`0.875rem`, `400 Regular`).
    *   Color: `Text Secondary` (`#6C757D`). Important entities like names or stages can be `Text Primary` or slightly bolder.
    *   Icons (Optional): A small icon preceding each entry to differentiate event types (e.g., feedback icon, stage change icon, application icon). Icon color `Text Secondary`.
    *   Separators: Subtle lines or just spacing between entries.
    *   Container: If the list is long, it could be scrollable within its container. Max height defined.

---

## 4. Right Column: The Feedback & Action Hub

This column consolidates all feedback and provides controls for progressing the candidate. It should be clear, actionable, and facilitate quick decision-making. Background: `Background Light` (`#FFFFFF`).

### Interviewers Section:

*   **Title:** "Assigned Interviewers" or "Interview Team."
    *   Styling: `H4` (`1.125rem`, `600 Semi-Bold`).
    *   Color: `Text Primary` (`#212529`).
*   **Layout:** A list of interviewers assigned to this candidate for the current job.
*   **Content for each interviewer:**
    *   **Name:** `Body Text` (`1rem`, `500 Medium`).
    *   **Avatar (optional):** Small circular avatar (`32px`).
    *   **Status Icon/Text:**
        *   "Feedback Pending": `Warning/In-Progress` color (`#FFC107`) icon (e.g., clock) and text.
        *   "Feedback Submitted": `Success/Positive` color (`#28A745`) icon (e.g., checkmark) and text.
        *   "Declined Invite": `Text Secondary` (`#6C757D`) icon (e.g., 'x' mark) and text.
        *   Text styling for status: `Small Text` (`0.875rem`).
    *   **Action - "Nudge" button (optional):**
        *   Appears next to "Feedback Pending" status.
        *   Styling: **Secondary Button** (small version). Text "Nudge".
            *   Padding: `0.25rem 0.5rem`.
            *   Font Size: `Small Text`.
*   **Card Styling (if each interviewer is a card):**
    *   Background: `Background Medium` (`#F8F9FA`).
    *   Padding: `0.75rem`. Corner Radius: `0.25rem`. Margin below each.

### Unified Feedback Dashboard:

*   **Title:** "Feedback Summary" or "Interview Feedback."
    *   Styling: `H3` (`1.375rem`, `600 Semi-Bold`) or `H4`.
    *   Color: `Text Primary`.
*   **Layout:** A list of feedback cards, one for each piece of submitted feedback.
*   **Individual Feedback Card Styling:**
    *   Background: `Background Light` (`#FFFFFF`) with a border `1px solid Background Dark` (`#E9ECEF`) OR `Background Medium` (`#F8F9FA`) with no border.
    *   Padding: `1rem`.
    *   Corner Radius: `0.375rem` (6px).
    *   Margin: `1rem` bottom margin between feedback cards.
*   **Content of each Feedback Card:**
    *   **Interviewer's Name & Avatar (optional):**
        *   Name Styling: `Body Text` (`1rem`, `600 Semi-Bold`).
        *   Avatar Size: `32px` or `40px`.
    *   **Date Submitted:** `Small Text` (`0.875rem`), `Text Secondary` (`#6C757D`).
    *   **Overall Recommendation:**
        *   Text: "Strong Hire," "Hire," "No Hire."
        *   Styling: Displayed prominently, perhaps as a tag or badge.
            *   Typography: `Body Text` (`1rem`, `700 Bold`) or `Small Text` (`0.875rem`, `700 Bold`) if part of a tag.
            *   "Strong Hire": Tag background `Success/Positive` (`#28A745`), Text `White` (`#FFFFFF`).
            *   "Hire": Tag background `Information` (`#17A2B8`) or a lighter green (e.g., `#A3D9A5`), Text `Text Primary` or `White`.
            *   "No Hire": Tag background `Danger/Alerts` (`#DC3545`) or `Background Dark` (`#E9ECEF`), Text `White` or `Text Primary`.
    *   **Structured Skill Ratings:**
        *   Layout: A list of predefined skills (e.g., "Problem Solving," "Technical Skill," "Communication," "Team Fit").
        *   Rating Display:
            *   "Problem Solving: 4/5" (Numerical display is clear and simple).
            *   Alternatively, use star icons (filled/empty) or a simple horizontal bar.
        *   Typography: Skill label `Body Text` (`1rem`, `400 Regular`), Rating `Body Text` (`1rem`, `600 Semi-Bold`).
    *   **Qualitative Comments/Notes:**
        *   Title: "Comments" or "Detailed Feedback." Styling: `H5` or bold `Body Text`.
        *   Content: Verbatim text from the interviewer.
        *   Styling: `Body Text` (`1rem`, `400 Regular`), `Text Primary`.
        *   Line Height: `1.5`.
        *   Expansion: If comments are very long (e.g., > 5 lines), truncate with a "Read More..." **Link Button**. Clicking expands the text in place.

### Action Buttons:

*   **Position:** Grouped together, typically at the bottom of the Right Column. Can be made "sticky" so they remain visible as the user scrolls through feedback.
*   **Available Buttons (Context-dependent, these are examples):**
    *   **"Move to Next Stage"**:
        *   Styling: **Primary Button** (`#007BFF` background, `White` text).
    *   **"Schedule Interview"**:
        *   Styling: **Primary Button** or **Secondary Button** (if "Move to Next Stage" is the more common primary action).
    *   **"Reject Candidate"**:
        *   Styling: **Secondary Button** but with `Danger/Alerts` color for text or border (`#DC3545`) to signify caution. Or, standard Secondary Button that triggers a confirmation modal with stronger warning colors.
        *   Confirmation: Must trigger a confirmation dialog (modal) before actioning. Modal should use `Danger/Alerts` color for its confirm button.
    *   **"Make Offer"**: (Appears at appropriate stage, e.g., post-interview and positive feedback)
        *   Styling: **Primary Button**.
*   **General Styling:** Use button styles defined in `STYLE_GUIDE.md`. Ensure sufficient spacing between buttons.

---
