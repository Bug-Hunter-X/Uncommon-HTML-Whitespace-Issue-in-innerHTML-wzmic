# Uncommon HTML Whitespace Issue in innerHTML

This repository demonstrates an uncommon HTML bug related to whitespace handling within the `innerHTML` property.  The bug specifically occurs when using `innerHTML` to inject content containing leading whitespace into a pre-existing HTML element.  Standard practices recommend using `textContent` for modifying text content, which typically avoids this issue.  However, this example highlights a scenario where `innerHTML` produces unexpected rendering results due to whitespace.

## Bug Description

The bug manifests as unexpected rendering behavior when updating the content of an HTML element using `innerHTML` and the new content contains a leading space in a paragraph tag.  The leading space is not handled correctly by the browser, leading to the paragraph being rendered differently than expected.

## How to Reproduce

1. Open `bug.html` in a web browser.
2. Observe the rendering of the paragraph that is updated using `innerHTML`. You'll note that the second paragraph has a space before it.

## Solution

The solution is to avoid leading spaces in the string that is being inserted into the HTML element using `innerHTML` or using `textContent` as suggested above. The solution file (`bugSolution.html`) demonstrates the corrected approach.
