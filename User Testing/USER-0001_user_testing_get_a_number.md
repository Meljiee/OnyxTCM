## **USER-0001:** User testing - Get a Number
> **Summary:** Verify that a user can request a ticket number to join a queue. <br>

**Preconditions:** User must be logged in and currently on the `User Dashboard` without an active ticket.

**Scenario 1**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Navigate to the main dashboard. | Verify that the `Not in a Queue yet?` screen is shown. |
| 2 | Tap the `Get a Number` button. | Verify that the system processes the request to join the queue. |
| 3 | Wait until the queue assignment is completed. | Verify that the `Active Ticket` screen is shown, displaying the assigned `Ticket Number` (e.g., "40"). |

**Post-conditions:**
- The user is added to the active queue and assigned a ticket number.
