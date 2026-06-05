## **USER-0006:** User testing - Real-Time Sync Validation
> **Summary:** Verify that the user's active ticket screen updates immediately via real-time listeners when the admin advances the queue. <br>

**Preconditions:** User is logged in and has an active ticket. Admin is logged in on a separate device or browser window.

**Scenario 1: Real-Time Queue Advance**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | **(User)** Keep the `Active Ticket` screen open and observe the `Current Position`. | Verify the starting position is displayed (e.g., "Position 5"). |
| 2 | **(Admin)** Navigate to the `Queue Management` screen. | Verify the admin interface is active. |
| 3 | **(Admin)** Tap the `Call Next` button. | Verify the admin UI updates the serving ticket. |
| 4 | **(User)** Observe the `Active Ticket` screen. | Verify that the `Current Position` automatically updates (e.g., drops to "Position 4") instantly without requiring the user to refresh the web page. |

**Post-conditions:**
- Client-side UI stays perfectly synchronized with backend database state changes.