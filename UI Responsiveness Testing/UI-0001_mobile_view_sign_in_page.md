# UI-0001: Mobile View - Sign In Page Layout Validation

## Summary

Verify that the unified login page dynamically adapts from a side-by-side split screen on desktop viewports into a vertically stacked configuration on mobile viewports.

**Preconditions:**

- The application is deployed live and reachable via `https://queuely-one.vercel.app/login`.

## Scenario 1: Responsive Stacking and Branding Position Shift

| #   | Step                                                                                                                                     | Expected Behavior                                                                                                                        |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Open the production login URL on a wide desktop viewport layout ($1440\text{px}$).                                                       | Verify that the page renders a horizontal split screen: branding panel with illustration on the left, login form card on the right.      |
| 2   | Right-click the page, open Developer Tools, and switch the viewport emulator to Mobile View (e.g., iPhone 12 Pro, $390\text{px}$ width). | Verify that the left-side branding illustration panel collapses seamlessly to prioritize the form interface.                             |
| 3   | Observe the topmost section of the mobile layout screen.                                                                                 | Verify that the **Queuely logo text and icon dynamically reposition to sit centered directly above the `Welcome Back` input form card**. |
| 4   | Inspect the interactive text field elements and buttons within the mobile view.                                                          | Verify that all input blocks and the primary `Sign In` button scale to full width (`w-full`) with comfortable padding parameters.        |

**Post-conditions:**

- The login layout scales cleanly without horizontal page clipping or obscured touch targets.
