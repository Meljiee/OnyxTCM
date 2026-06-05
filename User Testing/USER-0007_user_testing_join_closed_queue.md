## **USER-0007:** User testing - Join Closed Queue
> **Summary:** Verify that a user cannot generate a new ticket if the queue is currently closed or in maintenance mode. <br>

**Preconditions:** Admin has toggled the queue status to "Closed" or enabled "Maintenance Mode" in settings. User is logged in and on the dashboard.

**Scenario 1: Attempt to Join**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Navigate to the main dashboard. | Verify that the dashboard loads. |
| 2 | Observe the queue status indicator and action buttons. | Verify that a "Queue Closed" or "Maintenance" banner is visible. |
| 3 | Attempt to locate the `Get a Number` button. | Verify that the button is either entirely hidden from the UI, visually disabled (grayed out), or tapping it triggers a toast error stating "The queue is currently closed." |
| 4 | Verify ticket assignment. | Verify that no new ticket is generated and the user is not added to the database queue list. |

**Post-conditions:**
- The queue integrity is maintained while the system is closed.