# Blueprint: Curriculum Selection Simulator

## Overview

This document outlines the plan for creating a web-based "Curriculum Selection Simulator" for middle and high school students. The application will allow students to select subjects based on specific rules, track their required credits in real-time, and export their selections to an Excel file. The entire application will be built within a single HTML file for simplicity and ease of use.

## Core Features & Design

### 1. **Visual Design & Layout**

- **Sticky Credit Summary:** The credit summary panel at the top of the page will remain fixed (sticky) as the user scrolls, allowing for constant visibility of their credit status.
- **Grouped Table Layout:** The main curriculum table will be restructured for better readability:
    -   Subjects will be grouped under clear, high-level headers indicating the **Year, Semester, and selection rule** (e.g., "2학년 1학기 - 택4").
- **Action Buttons:** Two distinct buttons with icons (Print, Export) will be available at the bottom.

### 2. **Interactive Functionality**

- **Data-Driven:** The curriculum data is sourced from the official school document.
- **Complex Selection Rules:** The application enforces both required selections and choice-based rules (e.g., '택 N').
- **Real-time Credit Calculation:** The sticky summary panel will update in real-time.
- **Print & Export:** Clean, user-friendly printing and Excel exporting capabilities.

### 3. **Technical Implementation (Single `index.html`)**

- **HTML & CSS:** 
    -   `position: sticky` is used to fix the credit summary panel. The fix involves removing `overflow: hidden` from the parent `.container` class which was preventing the sticky behavior.
- **JavaScript:**
    -   The curriculum data is regularly updated and corrected based on user feedback to ensure accuracy.
    -   The `renderTable` function groups subjects by year and semester to create a clear, organized table structure.

## Plan for Current Request

1.  **Update `blueprint.md`:** Document the plan to fix the data error and the CSS `position: sticky` bug.
2.  **Modify `index.html`:**
    -   **CSS:** 
        -   In the `.container` style rule, remove the `overflow: hidden;` property to allow `position: sticky` to work correctly.
    -   **JavaScript (Data):** 
        -   Locate the '음악' and '미술' subject objects in the `curriculumData.subjects` array.
        -   Change the `year` property for both subjects from `2` to `1`.
        -   Assign '음악' to `semester: 1` and '미술' to `semester: 2`.
