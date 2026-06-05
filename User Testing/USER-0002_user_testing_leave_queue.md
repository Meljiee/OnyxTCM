## **USER-0002:** User testing - Leave Queue
> **Summary:** Verify that a user can successfully leave an active queue. <br>

**Preconditions:** User must be logged in and have an active ticket in a queue.

**Scenario 1**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Navigate to the `Active Ticket` screen. | Verify that the `Leave Queue` button is visible. |
| 2 | Tap the `Leave Queue` button. | Verify that the system processes the cancellation. |
| 3 | Wait until the cancellation is completed. | Verify that the `Not in a Queue yet?` dashboard screen is shown. |

**Post-conditions:**
- The user's ticket is cancelled and removed from the active queue.
