# CSS Specificity Bug: !important overriding nested selectors

This repository demonstrates a subtle bug related to CSS specificity and the `!important` declaration.  The bug arises when a nested selector attempts to override a style set with `!important` on a parent element.

## Bug Description

A common understanding of CSS specificity is that more specific selectors override less specific ones. However, the `!important` declaration overrides this behavior, even when dealing with nested selectors. This example showcases this unexpected interaction.

## How to Reproduce

1. Open `bug.css` and examine the provided CSS.
2. Create some HTML that incorporates the selectors (parent, child, grandchild).
3. Observe that the grandchild element inherits the style from the parent due to the `!important` flag, even though a more specific rule exists.

## Solution

The solution, located in `bugSolution.css`, illustrates how to avoid this unexpected behavior by carefully considering the use of `!important` and potentially restructuring the CSS to use more appropriate selectors or avoid the use of `!important` altogether.

## Conclusion

This example highlights the importance of understanding how `!important` affects CSS specificity and the potential for unexpected behavior when using it with nested selectors.  It's recommended to use `!important` sparingly and only when absolutely necessary.