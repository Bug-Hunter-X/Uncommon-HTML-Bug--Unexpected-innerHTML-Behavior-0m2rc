# Uncommon HTML Bug: Unexpected innerHTML Behavior

This repository demonstrates an uncommon bug related to the use of `innerHTML` in HTML.  The bug arises from potential timing issues and race conditions when repeatedly manipulating `innerHTML` within a script.

## Bug Description
The code attempts to append two paragraphs to a div element using `innerHTML`. However, due to the asynchronous nature of JavaScript execution, the second append might not render correctly or might fail entirely if there are timing issues between when innerHTML is set and when the dom is updated.

## Solution
The solution involves using DOM manipulation methods (`appendChild` and `createElement`) instead of directly modifying the `innerHTML`. This provides better control over the DOM structure and avoids the race condition.
