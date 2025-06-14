# Screen 4: Create New Job Form

This document outlines the design for the "Create New Job Form." It will be a full-page experience to accommodate multiple steps and fields comfortably. The design maintains consistency with other screens through the persistent Top Navigation Bar and references `STYLE_GUIDE.md` for visual styling.

## 1. Overall Layout & Access

*   **Access:** The form is accessed by clicking the "Create New Job" button (Primary Button style) in the persistent Top Navigation Bar.
*   **Page Structure:** Full-page layout.
*   **Persistent Top Navigation Bar:** The standard Top Navigation Bar as described in `SCREEN_MAIN_DASHBOARD.md` will be present at the top.
    *   The "Jobs" or "Dashboard" link might be shown as active, depending on the user's prior location before clicking "Create New Job."
*   **Page Title:**
    *   Content: "Create New Job Posting"
    *   Styling: `H1` (`2.25rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Position: Prominently displayed below the Top Navigation Bar, aligned to the left.
*   **Main Content Area Background:** `Background Light` (`#FFFFFF`). The form itself might be contained within a large card-like element with a `Background Light` or `Background Medium` fill and a subtle border, to give it structure on the page.

---

## 2. Form Structure (Multi-Step/Tabbed)

To make the form less daunting and easier to manage, a multi-step approach will be adopted.

*   **Progress Indicator:**
    *   Visual: A series of steps displayed horizontally below the page title (e.g., "Step 1: Job Details" -> "Step 2: Job Description" -> "Step 3: Assign Team & Review").
    *   Styling:
        *   Current Step: Highlighted using `Primary Accent` color (`#007BFF`) for text/icon and/or a stronger border/background for the step indicator. Font `Body Text` (`1rem`, `600 Semi-Bold`).
        *   Completed Steps: Can be indicated with a checkmark icon and `Success/Positive` color (`#28A745`) or a lighter shade of `Primary Accent`. Text `Body Text` (`1rem`, `400 Regular`).
        *   Upcoming Steps: Muted text color (`Text Secondary` (`#6C757D`)). Text `Body Text` (`1rem`, `400 Regular`).
        *   Connectors: Lines or chevrons between steps.
*   **Navigation Buttons (Button Bar):**
    *   A dedicated area at the bottom of the form for navigation buttons. This bar might have a `Background Medium` (`#F8F9FA`) fill or a top border to separate it from the form fields.
    *   **"Next Step" Button:**
        *   Styling: **Primary Button**.
        *   Visibility: Appears on Step 1 and Step 2.
    *   **"Previous Step" Button:**
        *   Styling: **Secondary Button** or **Link Button**.
        *   Visibility: Appears on Step 2 and Step 3.
    *   **"Save Draft" Button:**
        *   Styling: **Secondary Button**.
        *   Visibility: Available on all steps. Could be positioned to the left of "Next/Previous" buttons or in the top header of the form page. For simplicity, let's keep it in the bottom button bar.
    *   **"Publish Job" Button:**
        *   Styling: **Primary Button**.
        *   Visibility: Appears only on the final step (Step 3: Assign Team & Review) replacing the "Next Step" button.
*   **Content Area per Step:** Each step's content will be displayed below the progress indicator. The form will update this area when navigating between steps.

---

## 3. Step 1: Job Details

This step collects the fundamental information about the job posting.

*   **Step Title:** "Step 1: Job Details"
    *   Styling: `H2` (`1.75rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Position: Below the main page progress indicator.

### Fields:

*   **Job Title:**
    *   Label: "Job Title *"
    *   Input Type: Standard text input.
    *   Mandatory: Yes.
    *   Placeholder Text: "e.g., Senior Backend Engineer"
*   **Location:**
    *   Label: "Location *"
    *   Input Type: Radio buttons or a segmented control for "Remote," "On-site," "Hybrid."
        *   Styling: Radio buttons should follow standard web practices. Segmented control would be similar to the Job Status Toggle on Screen 2.
    *   Conditional Field: If "On-site" or "Hybrid" is selected:
        *   Label: "Work Address / City" (Can be optional or mandatory based on policy)
        *   Input Type: Standard text input.
        *   Placeholder Text: "e.g., San Francisco, CA or 123 Main St, New York"
*   **Department:**
    *   Label: "Department"
    *   Input Type: Standard text input or Select dropdown. A Select dropdown is preferable if there's a predefined list of departments.
        *   If Select: Options like "Engineering," "Marketing," "Sales," "Human Resources," etc.
    *   Placeholder Text (if text input): "e.g., Engineering"
    *   Mandatory: No (unless company policy dictates).
*   **Employment Type:**
    *   Label: "Employment Type *"
    *   Input Type: Select dropdown.
    *   Options: "Full-time," "Part-time," "Contract," "Temporary," "Internship."
    *   Mandatory: Yes.
*   **Experience Level:**
    *   Label: "Experience Level *"
    *   Input Type: Select dropdown.
    *   Options: "Entry-Level," "Associate," "Mid-Level," "Senior," "Lead," "Principal," "Manager."
    *   Mandatory: Yes.
*   **Salary Range (Optional):**
    *   Section Label: "Salary Range (Optional)" - `H4` or bold `Body Text`.
    *   Input Type:
        *   Option 1 (Separate Min/Max):
            *   Label Min: "Minimum Salary" - Text input. Placeholder "e.g., $100,000".
            *   Label Max: "Maximum Salary" - Text input. Placeholder "e.g., $150,000".
        *   Option 2 (Single Range Field):
            *   Label: "Salary Range" - Text input. Placeholder "e.g., $100,000 - $150,000 per year".
    *   Currency Selector: Select dropdown next to salary fields (e.g., USD, EUR, CAD). Defaults to company's primary currency.
    *   Checkbox:
        *   Label: "Do not display salary to candidates."
        *   Styling: Standard checkbox.
    *   Helper Text: "Providing a salary range can attract more qualified candidates." - `Small Text`, `Text Secondary`.

### General Styling for Step 1:

*   **Labels:** `Body Text` (`1rem`, `600 Semi-Bold` or `500 Medium`) from `STYLE_GUIDE.md`. Positioned above their respective input fields. Color `Text Primary`.
*   **Input Fields (Text, Select):**
    *   Height: Consistent (e.g., 40-44px).
    *   Padding: `0.5rem 0.75rem`.
    *   Border: `1px solid Background Dark` (`#E9ECEF`).
    *   Corner Radius: `0.25rem` or `0.375rem` (4px or 6px).
    *   Focus State: Border color changes to `Primary Accent` (`#007BFF`), and a subtle box shadow using `Primary Accent` might appear.
    *   Background: `Background Light` (`#FFFFFF`).
    *   Text: `Body Text` (`1rem`, `400 Regular`), `Text Primary`.
*   **Required Fields:** Marked with an asterisk (*) next to the label.
*   **Layout:** Single column layout for fields is generally clearest. Two columns could be used for very short, related fields like Min/Max salary if desired, but ensure proper alignment and spacing.
*   **Spacing:** Adequate vertical spacing between field groups (e.g., `1rem` to `1.5rem`).

---

## 4. Step 2: Job Description

This step focuses on the qualitative aspects of the job, providing candidates with a detailed understanding of the role.

*   **Step Title:** "Step 2: Job Description"
    *   Styling: `H2` (`1.75rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).
    *   Position: Below the main page progress indicator.

### Fields:

*   **Main Description/Overview:**
    *   Label: "Job Overview / Summary *"
    *   Input Type: Rich-text editor (WYSIWYG).
        *   Controls: Standard toolbar with Bold, Italic, Underline, Bullet Lists (ul), Numbered Lists (ol), Links. Possibly font size/heading options if deemed necessary, but simplicity is key.
        *   Min Height: e.g., `200px` or `250px`.
        *   Styling: The editor's chrome (toolbar, border) should be clean. Border `1px solid Background Dark` (`#E9ECEF`). Focus state can highlight the border with `Primary Accent`.
    *   Mandatory: Yes.
    *   Helper Text: "Provide a compelling overview of the role and company culture." (`Small Text`, `Text Secondary`).
*   **Responsibilities:**
    *   Label: "Key Responsibilities *"
    *   Input Type: Rich-text editor or a simple textarea. If textarea, explicitly state "Use bullet points for clarity."
        *   If Rich-text: Same controls as Main Description, possibly a more compact version.
        *   Min Height: e.g., `150px`.
    *   Mandatory: Yes.
    *   Placeholder Text (if textarea):
        ```
        - Develop and maintain web applications...
        - Collaborate with cross-functional teams...
        - Write clean, scalable code...
        ```
*   **Qualifications/Requirements:**
    *   Label: "Qualifications / Requirements *"
    *   Input Type: Rich-text editor or a simple textarea.
        *   Min Height: e.g., `150px`.
    *   Mandatory: Yes.
    *   Placeholder Text (if textarea):
        ```
        - Bachelor's degree in Computer Science or related field...
        - 5+ years of experience in [Technology]...
        - Strong understanding of [Concept]...
        ```
*   **Benefits (Optional):**
    *   Label: "Benefits & Perks"
    *   Input Type: Rich-text editor or a simple textarea.
        *   Min Height: e.g., `100px`.
    *   Mandatory: No.
    *   Placeholder Text (if textarea): "e.g., Competitive salary, Health insurance, Paid time off, Remote work options..."

### Template Suggestion:

*   **Button/Link:** "Use a Job Description Template"
    *   Styling: **Secondary Button** (outline style) or a prominent **Link Button**.
    *   Position: Near the top of this step, perhaps below the "Step 2" title or to the right.
    *   Action: Opens a modal dialog.
*   **Modal Content:**
    *   Title: "Job Description Templates"
    *   Layout: A list of available templates (e.g., "Software Engineer," "Product Manager," "Sales Representative"). Could be searchable or categorized.
    *   Interaction: Selecting a template would populate the fields in Step 2 (Main Description, Responsibilities, Qualifications) with the template content. A "Preview" option could be useful.
    *   Confirmation: "Using a template will replace any existing content in the job description fields. Are you sure?"

### General Styling for Step 2:

*   **Labels:** Same as Step 1 (`Body Text`, `600 Semi-Bold` or `500 Medium`, `Text Primary`, above fields).
*   **Rich-Text Editors:**
    *   Should have a clear visual boundary.
    *   Font inside the editor should be `Body Text` from `STYLE_GUIDE.md`.
*   **Spacing:** Ample spacing between the large text areas (`1.5rem`).

---

## 5. Step 3: Assign Team & Review

This final step allows for assigning team members responsible for the hiring process and provides a comprehensive review of all entered information before publishing.

*   **Step Title:** "Step 3: Assign Team & Review"
    *   Styling: `H2` (`1.75rem`, `700 Bold`) from `STYLE_GUIDE.md`.
    *   Color: `Text Primary` (`#212529`).

### Assign Team Members:

*   **Assign Hiring Manager (Optional but Recommended):**
    *   Label: "Hiring Manager"
    *   Input Type: Select dropdown.
    *   Options: Populated with a list of existing users/team members in the Nexus HR system (e.g., "Priya Sharma," "Rohan Kumar").
    *   Helper Text: "The hiring manager is typically responsible for the final hiring decision." (`Small Text`, `Text Secondary`).
*   **Assign Interviewers (Optional):**
    *   Label: "Interviewers"
    *   Input Type: Multi-select dropdown with search/filtering capabilities or a checklist of users.
    *   Options: Populated with existing users.
    *   Helper Text: "Select team members who will be involved in interviewing candidates. You can always assign or change interviewers later from the job's dashboard." (`Small Text`, `Text Secondary`).

### Review Section:

*   **Title:** "Review Your Job Posting"
    *   Styling: `H3` (`1.375rem`, `600 Semi-Bold`).
    *   Layout: A read-only summary of all information entered in Step 1 and Step 2.
*   **Content Structure:**
    *   **Job Details (from Step 1):**
        *   Section Title: "Job Details" (`H4`).
        *   Display: Each field (Job Title, Location, Department, Employment Type, Experience Level, Salary Range) with its entered value. Labels styled as bold `Body Text`, values as regular `Body Text`.
    *   **Job Description (from Step 2):**
        *   Section Title: "Job Description" (`H4`).
        *   Display: The content from Main Description, Responsibilities, Qualifications, and Benefits sections. This content should be rendered to reflect the formatting applied in the rich-text editors (e.g., bold, lists).
*   **"Edit" Links:**
    *   Next to each section title (e.g., "Job Details [Edit]") or for each major block of information, provide a "Edit" link/button (styled as a `Link Button`).
    *   Action: Clicking "Edit" takes the user directly back to the relevant step and fieldset to make changes.

### Action Buttons on this final step (in the bottom button bar):

*   **"Publish Job"**:
    *   Styling: **Primary Button**. Replaces "Next Step".
    *   Action: Submits the form, creates the job posting, makes it active (or pending approval if such a workflow exists). Navigates to the newly created Job's dashboard/pipeline view (Screen 2).
*   **"Save Draft"**:
    *   Styling: **Secondary Button**.
    *   Action: Saves all current information as a draft. User might be taken to a "Drafts" list or back to the main dashboard.
*   **"Previous Step"**:
    *   Styling: **Secondary Button** or **Link Button**.
    *   Action: Navigates to Step 2.

---

## 6. General Form Styling & Interactions (Applicable to all steps)

*   **Input Fields (General):**
    *   Refer to `STYLE_GUIDE.md` and specific step styling.
    *   Disabled State: Light gray background (`Background Dark` or a lighter version), `Text Secondary` color, `not-allowed` cursor.
*   **Labels:**
    *   Position: Consistently above their respective input fields.
    *   Required Fields: Clearly marked with an asterisk (*) after the label text (e.g., "Job Title *").
*   **Helper Text / Instructions:**
    *   Used for fields that might need clarification.
    *   Styling: `Small Text` (`0.875rem`), `Text Secondary` (`#6C757D`), positioned below the relevant input field.
*   **Error Handling & Validation:**
    *   Client-side validation should occur before allowing navigation to the next step or on attempting to publish.
    *   **Field Error Indication:**
        *   Input Border: Changes to `Danger/Alerts` color (`#DC3545`).
        *   Error Message: A clear message appears below the field.
            *   Styling: `Small Text` (`0.875rem`), color `Danger/Alerts` (`#DC3545`).
            *   Icon: Optionally, a small warning icon can precede the error message.
    *   **Summary Error Message (Optional):** If form submission fails, a summary message can appear at the top of the form or step, listing the fields that require attention.
*   **Button Bar:**
    *   Position: Fixed at the bottom of the form content area or scrolls with the page but always clearly separated.
    *   Layout: Buttons aligned to the right, or "Save Draft" on the left and "Previous/Next/Publish" on the right.
    *   Disabled Buttons: If a "Next" or "Publish" button is disabled until all required fields are filled, it should use the disabled button style from `STYLE_GUIDE.md` (lighter background, muted text).

---
