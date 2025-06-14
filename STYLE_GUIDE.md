# Nexus HR Portal Style Guide

## 1. Color Palette

The color palette is designed to be professional, clean, and accessible, reflecting the brand keywords of "modern," "efficient," and "user-friendly."

### Base Colors:
*   **Background Light:** `#FFFFFF` (White) - Provides a clean and spacious feel.
*   **Background Medium:** `#F8F9FA` (Light Gray) - Used for subtle differentiation of sections or elements.
*   **Background Dark:** `#E9ECEF` (Slightly Darker Gray) - Can be used for borders or disabled states.
*   **Text Primary:** `#212529` (Near Black) - Ensures high readability for body text.
*   **Text Secondary:** `#6C757D` (Dark Gray) - For less prominent text or captions.

### Accent Colors:
*   **Primary Accent:** `#007BFF` (Professional Blue) - Chosen for its professional and trustworthy feel, suitable for interactive elements and calls to action. This aligns with the "efficient" and "modern" keywords.
*   **Primary Accent Hover:** `#0056b3` (Darker Blue) - For hover states on primary interactive elements.
*   **Primary Accent Active:** `#004085` (Even Darker Blue) - For active states on primary interactive elements.

### Status Indicators:
*   **Success/Positive:** `#28A745` (Green) - Universally recognized for positive outcomes (e.g., "Hired," "Approved").
*   **Warning/In-Progress:** `#FFC107` (Yellow) - Indicates caution or an ongoing process (e.g., "In Progress," "Pending Review").
*   **Danger/Alerts:** `#DC3545` (Red) - Used for critical alerts, errors, or negative outcomes (e.g., "Rejected," "Error").
*   **Information:** `#17A2B8` (Teal) - For informational messages or highlights that are not status-critical.

---

## 2. Typography

The typography is chosen for its readability and modern aesthetic, contributing to a user-friendly and efficient interface.

### Font Family:
*   **Primary Font:** `Inter` (or a readily available sans-serif like Arial, Helvetica Neue, sans-serif as a fallback) - Inter is a clean, modern, and highly readable sans-serif font that works well for UI design and various text sizes. It supports the "modern" and "user-friendly" brand aspects.

### Font Sizes and Weights:

*   **H1 (Page Titles):**
    *   Font Size: `2.25rem` (36px)
    *   Font Weight: `700` (Bold)
    *   Line Height: `1.2`
*   **H2 (Section Titles):**
    *   Font Size: `1.75rem` (28px)
    *   Font Weight: `700` (Bold)
    *   Line Height: `1.2`
*   **H3 (Sub-Section Titles):**
    *   Font Size: `1.375rem` (22px)
    *   Font Weight: `600` (Semi-Bold)
    *   Line Height: `1.3`
*   **H4 (Card Titles/Important Labels):**
    *   Font Size: `1.125rem` (18px)
    *   Font Weight: `600` (Semi-Bold)
    *   Line Height: `1.4`
*   **Body Text (Default Paragraphs, Lists):**
    *   Font Size: `1rem` (16px)
    *   Font Weight: `400` (Regular)
    *   Line Height: `1.5`
*   **Small Text (Captions, Helper Text):**
    *   Font Size: `0.875rem` (14px)
    *   Font Weight: `400` (Regular)
    *   Line Height: `1.4`
*   **Button Text:**
    *   Font Size: `1rem` (16px)
    *   Font Weight: `500` (Medium) or `600` (Semi-Bold) - depending on button hierarchy.

---

## 3. Button Styles

Button styles are designed to be clear, consistent, and provide obvious visual feedback to the user, reinforcing the "efficient" and "user-friendly" nature of the portal.

### Primary Button
Used for main calls to action (e.g., "Create New Job," "Move to Next Stage," "Submit").

*   **Background Color:** `Primary Accent` (`#007BFF`)
*   **Text Color:** `#FFFFFF` (White)
*   **Border:** None
*   **Padding:** `0.75rem 1.5rem` (12px 24px) - Provides a comfortable click target.
*   **Corner Radius:** `0.375rem` (6px) - Slightly rounded corners for a modern look.
*   **Font Weight:** `600` (Semi-Bold)
*   **Hover State:**
    *   Background Color: `Primary Accent Hover` (`#0056b3`)
    *   Text Color: `#FFFFFF`
*   **Active State:**
    *   Background Color: `Primary Accent Active` (`#004085`)
    *   Text Color: `#FFFFFF`
    *   Transform: `scale(0.98)` or subtle inset box-shadow.
*   **Disabled State:**
    *   Background Color: `#A0CFFF` (Lighter version of Primary Accent) or `Background Dark` (`#E9ECEF`)
    *   Text Color: `#6C757D` (Text Secondary) or `#BDC3C7` (Light Gray)
    *   Cursor: `not-allowed`

### Secondary Button
Used for less critical actions that are still important (e.g., "Edit Job," "Cancel," "View Details").

*   **Background Color:** `#FFFFFF` (White) or `transparent`
*   **Text Color:** `Primary Accent` (`#007BFF`)
*   **Border:** `1px solid` `Primary Accent` (`#007BFF`)
*   **Padding:** `0.75rem 1.5rem` (12px 24px)
*   **Corner Radius:** `0.375rem` (6px)
*   **Font Weight:** `600` (Semi-Bold)
*   **Hover State:**
    *   Background Color: `Primary Accent` (`#007BFF`)
    *   Text Color: `#FFFFFF`
    *   Border Color: `Primary Accent` (`#007BFF`)
*   **Active State:**
    *   Background Color: `Primary Accent Active` (`#004085`)
    *   Text Color: `#FFFFFF`
    *   Border Color: `Primary Accent Active` (`#004085`)
    *   Transform: `scale(0.98)` or subtle inset box-shadow.
*   **Disabled State:**
    *   Background Color: `#FFFFFF` or `Background Dark` (`#E9ECEF`)
    *   Text Color: `#A0CFFF` (Lighter version of Primary Accent) or `#BDC3C7`
    *   Border Color: `#A0CFFF` (Lighter version of Primary Accent) or `#CED4DA`
    *   Cursor: `not-allowed`

### Link Buttons
Text that functions as a button, typically used for navigation or minor inline actions (e.g., "Advanced Search," "Clear Filters").

*   **Text Color:** `Primary Accent` (`#007BFF`)
*   **Background Color:** `transparent`
*   **Border:** None
*   **Padding:** `0.25rem 0.5rem` (or as needed for click target)
*   **Font Weight:** `500` (Medium)
*   **Text Decoration:** None (by default)
*   **Hover State:**
    *   Text Color: `Primary Accent Hover` (`#0056b3`)
    *   Text Decoration: `underline`
*   **Active State:**
    *   Text Color: `Primary Accent Active` (`#004085`)
    *   Text Decoration: `underline`
*   **Disabled State:**
    *   Text Color: `#A0CFFF` (Lighter version of Primary Accent) or `#BDC3C7`
    *   Cursor: `not-allowed`
    *   Text Decoration: `none`

---
