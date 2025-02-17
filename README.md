# CSS calc() Bug with Percentage and Undefined Parent Dimensions

This repository demonstrates a common, yet easily overlooked, issue when using the `calc()` function in CSS with percentage values. The problem arises when the parent container's dimensions are not explicitly defined, leading to incorrect calculations.

**Problem:** The `calc()` function relies on the context of the parent element to resolve percentage values. If the parent doesn't have a defined width or height, the calculation fails to produce the expected output.

**Example:**
Consider a child element attempting to calculate its width as `50% - 10px`. If the parent has no explicit width, the `50%` resolves to an undefined value, resulting in incorrect results. 

**Solution:** Always ensure that parent containers have their dimensions explicitly defined (using `width`, `height`, etc.) before using percentage-based `calc()` calculations within child elements. 

**Files:**
- `bug.css`: Demonstrates the buggy behavior
- `bugSolution.css`: Provides the corrected CSS with explicit parent container dimensions. 