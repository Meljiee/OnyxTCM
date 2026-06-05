## **USER-0004:** User testing - View Active Ticket Details
> **Summary:** Verify that the active ticket screen correctly displays queue position, estimated wait time, and queue updates. <br>

**Preconditions:** User must be logged in and have an active ticket in a queue.

**Scenario 1**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Navigate to the main dashboard with an active ticket. | Verify that the `Active Ticket` screen is shown. |
| 2 | Observe the `Current Position` section. | Verify that the user's current position and the total number of people in line are displayed accurately. |
| 3 | Observe the `Estimated Time Wait` section. | Verify that the estimated wait time in minutes and the approximate service time are displayed. |
| 4 | Observe the `Queue Updates` section at the bottom. | Verify that recent notifications (e.g., "You've been added to the end of the queue.") are visible. |

**Post-conditions:**
- The user is accurately informed of their real-time status in the queue.
