# Unclosed Paragraph Tags in innerHTML

This example demonstrates an uncommon HTML bug that arises from using `innerHTML` with an incompletely formed string.  Improperly closing HTML tags within the string assigned to `innerHTML` can result in unexpected rendering issues.

The bug occurs because the browser attempts to parse the malformed HTML.  The lack of proper closing tags prevents the browser from correctly interpreting the structure, potentially affecting display and potentially causing follow-on JavaScript errors if the incomplete tags attempt to reference DOM objects.

## How to Reproduce

1. Open `bug.html` in a web browser.
2. Observe the missing text from the div; only part of the content renders.

## Solution

The solution is simple: ensure all tags are properly closed within the string used to set `innerHTML`.

Review `bugSolution.html` for a corrected version of the code.