# Uncommon HTML Bug: Element Not Found

This repository demonstrates a subtle bug that can occur in HTML when a script attempts to access a DOM element before it has been fully parsed and added to the DOM tree.  The `document.getElementById` method returns `null` if the element hasn't been parsed yet. This can happen if the script is placed before the target element in the HTML or if the element's creation involves asynchronous processes.

The `bug.html` file showcases the problematic code; `bugSolution.html` provides a correct implementation using DOMContentLoaded.

## How to reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Observe that the script fails to replace the text because `myDiv` is not found (in some browsers it might work).
4. Open `bugSolution.html` to see the corrected version.