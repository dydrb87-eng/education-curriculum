
# Blueprint: Curriculum Selection Simulator

## Overview

This document outlines the plan for creating a web-based "Curriculum Selection Simulator" for middle and high school students. The application will allow students to select subjects based on specific rules, track their required credits in real-time, and export their selections to an Excel file. The entire application will be built within a single HTML file for simplicity and ease of use.

## Core Features & Design

### 1. **Visual Design & Layout**

- **Sticky Credit Summary:** The credit summary panel at the top of the page will remain fixed (sticky) as the user scrolls, allowing for constant visibility of their credit status.
- **Grouped Table Layout:** The main curriculum table will be restructured for better readability:
    -   Subjects will be grouped under clear, high-level headers indicating the **Year, Semester, and selection rule** (e.g., "2학년 1학기 - 택4").
- **Action Buttons:** Two distinct buttons with icons (Print, Export) will be available at the bottom.
- **Clearer Terminology:** Renamed table headers for better clarity: "과목" is now "과목군" and "과목 정보" is now "과목명".

### 2. **Interactive Functionality**

- **Data-Driven:** The curriculum data is sourced from the official school document.
- **Complex Selection Rules:** The application enforces both required selections and choice-based rules (e.g., '택 N').
- **Real-time Credit Calculation:** The sticky summary panel will update in real-time.
- **Print & Export:** Clean, user-friendly printing and Excel exporting capabilities.
- **Add Subject:** Users can add custom subjects to each semester.
- **Unlockable Required Subjects:** School-designated required subjects are now unlockable, allowing for more flexible simulation.

### 3. **Technical Implementation (Single `index.html`)**

- **HTML & CSS:** 
    -   `position: sticky` is used to fix the credit summary panel. The fix involves removing `overflow: hidden` from the parent `.container` class which was preventing the sticky behavior.
    -   A modal (popup) is implemented for the "Add Subject" feature.
- **JavaScript:**
    -   The curriculum data is regularly updated and corrected based on user feedback to ensure accuracy.
    -   The `renderTable` function groups subjects by year and semester to create a clear, organized table structure.
    -   Event listeners are added for the "Add Subject" button and modal interactions.
    -   The `disabled` attribute is removed from the checkboxes for required subjects to allow for user interaction.

## Plan for Current Request

1.  **Update `blueprint.md`:** Document the plan to rename the table headers.
2.  **Modify `index.html`:**
    -   **HTML (Table Header):** 
        -   Change `<th>과목</th>` to `<th>과목군</th>`.
        -   Change `<th>과목 정보</th>` to `<th>과목명</th>`.
    -   **HTML (Modal):** 
        -   Update placeholder text in the "Add Subject" modal to reflect the new terminology (e.g., "과목군" and "과목명").

