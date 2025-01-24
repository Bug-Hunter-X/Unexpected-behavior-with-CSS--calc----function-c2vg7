# Unexpected Behavior with CSS `calc()` Function

This repository demonstrates an uncommon issue that can arise when using the `calc()` function in CSS, specifically within a flexbox container.  The `calc()` function is powerful, but subtle errors in usage can lead to unexpected results.

The `bug.css` file contains the problematic CSS, while `bugSolution.css` provides a corrected version.

The problem occurs because `calc()` operates on the available space differently depending on the context.   It is essential to understand that the subtraction in `calc(100% - 10px)` happens on the *available* space, not necessarily the parent container's space.  With flexbox, the available space can change based on content size and distribution.