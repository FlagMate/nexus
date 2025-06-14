# Screen 1: Main Dashboard Design

This document describes the design for the Main Dashboard of the Nexus HR Portal, referencing `STYLE_GUIDE.md` for visual styling.

## 1. Overall Layout

The Main Dashboard will feature a spacious and uncluttered layout, emphasizing a clear visual hierarchy. The design will make extensive use of whitespace and card-based elements to organize information, aligning with the "modern" and "user-friendly" brand keywords.

*   **Header (Persistent Top Navigation Bar):** A fixed bar at the top of the page providing consistent navigation and primary actions.
*   **Main Content Area:** Below the header, this area will house various widgets and information blocks, dynamically displaying key information relevant to the user. The layout will be a single column on mobile, potentially expanding to two or three columns on wider screens for widgets like Stat Cards and Active Jobs.

---

## 2. Top Navigation Bar (Persistent)

The top navigation bar will be present on all screens, providing global navigation and quick access to essential functions. It will use `Background Light` (`#FFFFFF`) with a subtle bottom border using `Background Dark` (`#E9ECEF`) for separation from the main content.

### Left Side:

*   **Logo:**
    *   Content: Placeholder text "Nexus" or a simple logo graphic.
    *   Styling: Positioned to the far left. Font style should be distinct, possibly using `H3` size (`1.375rem`, `600 Semi-Bold`) with `Text Primary` color (`#212529`).
*   **Navigation Links:**
    *   Links: "Dashboard" (active), "Jobs," "Candidates," "Team."
    *   Styling:
        *   Arranged horizontally next to the logo.
        *   Uses **Link Button** style from `STYLE_GUIDE.md`.
            *   Text Color: `Primary Accent` (`#007BFF`).
            *   Active Link ("Dashboard"): `Text Primary` (`#212529`) or a slightly bolder version of `Primary Accent`, with a subtle underline or bottom border using `Primary Accent`.
            *   Hover State: Text Color `Primary Accent Hover` (`#0056b3`), `underline`.
            *   Padding: `0.5rem 1rem` for adequate spacing.
            *   Font Weight: `500` (Medium).

### Right Side:

*   **"Create New Job" Button:**
    *   Styling: Uses **Primary Button** style from `STYLE_GUIDE.md`.
        *   Background Color: `Primary Accent` (`#007BFF`).
        *   Text Color: `#FFFFFF` (White).
        *   Padding: `0.5rem 1rem` (slightly smaller for a nav bar button, or use the standard `0.75rem 1.5rem` if space permits and it looks balanced).
        *   Corner Radius: `0.375rem` (6px).
        *   Font Weight: `600` (Semi-Bold).
*   **Notification Bell Icon:**
    *   Appearance: A standard bell icon (e.g., from an icon library).
    *   Color: `Text Secondary` (`#6C757D`) when no new notifications. Changes to `Primary Accent` (`#007BFF`) when new notifications are present.
    *   Badge: A small red dot (`Danger/Alerts` color `#DC3545`) or a number count badge will appear on the top-right of the icon if there are unread notifications.
    *   Interaction: Clicking the icon will open a dropdown list of recent notifications.
*   **User Profile Dropdown:**
    *   Appearance: Displays "Priya" (user's first name) and a small circular user avatar/icon.
        *   Text Style: `Body Text` (`1rem`, `400 Regular`) using `Text Primary` (`#212529`).
        *   Avatar: A simple circular placeholder with initials or a generic profile icon.
    *   Interaction: Clicking on the name or avatar.
        *   Action: Opens a dropdown menu.
        *   Dropdown Menu Styling: `Background Light` (`#FFFFFF`) with a light shadow.
        *   Dropdown Links: "Profile," "Settings," "Logout." Styled similarly to `Link Buttons` but typically smaller font size (`Small Text` or `Body Text`) and full width within the dropdown.
            *   Hover State for Dropdown Links: Subtle `Background Medium` (`#F8F9FA`) for the link area.

---

## 3. Main Content Area

The main content area is designed to provide Priya with an at-a-glance overview of key information and pending tasks. It will utilize cards and clear typography for readability and quick scanning.

### Welcome Widget:

*   **Text:** "Good Morning, Priya." (Greeting can be dynamic based on the time of day: "Good Afternoon," "Good Evening").
*   **Styling:**
    *   Typography: `H2` (`1.75rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Tone: Prominent yet friendly, positioned at the top of the main content area.
    *   Spacing: Adequate margin below to separate it from the subsequent widgets.

### Freemium Plan Status:

*   **Display Text Example:** "Jobs Posted: 7 / 100 Total. Active Jobs: 4 / 10 Parallel." (Numbers should be dynamic).
*   **Styling:**
    *   Typography: `Small Text` (`0.875rem`, `400 Regular`) or `Body Text` (`1rem`, `400 Regular`) from `STYLE_GUIDE.md`.
    *   Color: `Text Secondary` (`#6C757D`).
    *   Layout: Displayed as a single line of text directly below the Welcome Widget or to its right on wider screens.
    *   Visual Treatment: To make it distinct but not dominant, it could be placed within a very light gray (`Background Medium` `#F8F9FA`) padded box with small corner radii (`0.25rem`), or simply have a top/bottom border using `Background Dark` (`#E9ECEF`) if not boxed. It should not compete visually with primary action elements.
    *   Non-intrusive: The goal is to inform, not to be a primary call to action.

### High-Level Stats (Stat Cards):

*   **Content:**
    *   Card 1: "Total Active Jobs" (e.g., "12")
    *   Card 2: "New Candidates This Week" (e.g., "45")
    *   Card 3: "Pending Feedback" (e.g., "3")
*   **Layout:**
    *   Arranged in a horizontal row, typically 3 cards across on desktop/tablet views. On mobile, they would stack vertically.
    *   Sufficient spacing between cards to maintain an uncluttered look.
*   **Card Styling (Individual Card):**
    *   Background: `Background Light` (`#FFFFFF`) with a subtle border (e.g., `1px solid Background Dark` (`#E9ECEF`)) OR `Background Medium` (`#F8F9FA`) with no border.
    *   Padding: Generous padding (e.g., `1rem` or `1.5rem`).
    *   Corner Radius: `0.375rem` (6px) or `0.5rem` (8px) for a slightly softer modern look.
    *   Shadow: Subtle box shadow to lift the cards off the page (optional, but enhances the "card" feel).
    *   **Statistic Number:**
        *   Typography: Large and prominent, e.g., `H1` (`2.25rem`, `700 Bold`) or a custom large size like `2.5rem`.
        *   Color: `Primary Accent` (`#007BFF`) or `Text Primary` (`#212529`).
    *   **Label Text:**
        *   Typography: `Body Text` (`1rem`, `400 Regular`) or `Small Text` (`0.875rem`, `400 Regular`).
        *   Color: `Text Secondary` (`#6C757D`).
        *   Position: Directly below the statistic number.
    *   **Icon (Optional):**
        *   A minimalist icon associated with each stat (e.g., briefcase for jobs, users for candidates, speech bubble for feedback).
        *   Color: `Text Secondary` (`#6C757D`) or a lighter shade of `Primary Accent`.
        *   Size: `1.5rem` to `2rem`.
        *   Position: Typically to the right of the text/number, or above the label.
    *   **Interaction:** These cards are primarily informational but could link to a filtered view on the relevant page (e.g., "Total Active Jobs" card links to the "Jobs" page). If interactive, a hover state (e.g., slightly darker border or shadow) should be defined.

### "My Tasks" / "Needs Action" Widget:

*   **Layout:** A distinct card or section with a clear title. Can span full width or be part of a multi-column layout on larger screens.
*   **Title:** "My Tasks" or "Needs Your Attention."
    *   Styling: `H3` (`1.375rem`, `600 Semi-Bold`) or `H4` (`1.125rem`, `600 Semi-Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
*   **Item Examples:**
    *   "Review 5 new applicants for the 'Senior Backend Engineer' role."
    *   "Feedback is due from Rohan for Anjali Sharma's interview."
    *   "Schedule interview for Vikram Singh."
*   **Item Styling:**
    *   List Format: Each task presented as a list item.
    *   Typography: `Body Text` (`1rem`, `400 Regular`) for the main task description.
    *   Color: `Text Primary` (`#212529`).
    *   Interactivity: Parts of the task description that are actionable (e.g., job title, candidate name) should be styled as links.
        *   Link Styling: Use **Link Button** style (`Primary Accent` text color, `underline` on hover) from `STYLE_GUIDE.md`.
    *   Separators: Subtle horizontal lines (`1px solid Background Dark` (`#E9ECEF`)) between tasks.
    *   Padding: Adequate padding for each list item (`0.5rem 0`).
    *   Priority Indicators (Optional): A small colored dot or icon next to a task to indicate urgency (e.g., red for high priority), using `Status Indicator` colors.
*   **Card Styling:**
    *   Background: `Background Light` (`#FFFFFF`) with a subtle border OR `Background Medium` (`#F8F9FA`).
    *   Padding: `1rem` or `1.5rem`.
    *   Corner Radius: `0.375rem` (6px).

### Active Jobs Overview:

*   **Layout:** A list or a series of cards, displayed below the Stat Cards or My Tasks widget.
*   **Title:** "Active Jobs."
    *   Styling: `H3` (`1.375rem`, `600 Semi-Bold`) or `H4` (`1.125rem`, `600 Semi-Bold`).
    *   Color: `Text Primary` (`#212529`).
    *   "View All" Link: Optionally, a "View All Jobs" link styled as a `Link Button` can be placed to the right of the title.
*   **Card/List Item Content (for each job):**
    *   **Job Title:** (e.g., "Senior Backend Engineer")
        *   Styling: `H4` (`1.125rem`, `600 Semi-Bold`) or bolded `Body Text`.
        *   Color: `Primary Accent` (`#007BFF`) to indicate it's a link.
        *   Interaction: Clicking takes the user to the "Single Job View" for that specific job.
        *   Hover State: Text underline or slightly brighter `Primary Accent Hover`.
    *   **Number of Candidates:** (e.g., "15 Candidates")
        *   Styling: `Small Text` (`0.875rem`, `400 Regular`).
        *   Color: `Text Secondary` (`#6C757D`).
        *   Position: Below the job title.
    *   **Progress Bar (Optional):**
        *   Visual: A thin horizontal bar representing the pipeline progress (e.g., % shortlisted, % interviewing).
        *   Height: `0.25rem` to `0.5rem` (4px to 8px).
        *   Background: `Background Dark` (`#E9ECEF`).
        *   Fill Color: `Primary Accent` (`#007BFF`).
        *   Labeling: May include small text labels for stages if space allows, or on hover.
        *   Position: Below the candidate count or alongside it.
*   **Card/List Item Styling:**
    *   Background: `Background Light` (`#FFFFFF`) with a subtle border OR `Background Medium` (`#F8F9FA`).
    *   Padding: `1rem`.
    *   Corner Radius: `0.375rem` (6px).
    *   Spacing: Margin between cards/list items.
    *   Hover State (for the whole card if not just the title is clickable): Subtle shadow increase or border highlight.

---
