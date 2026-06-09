## **ADM-0002:** Admin testing - Queue Controls

> **Summary:** Verify that the admin can manage the active queue using the Call Next, Complete Service, and Skip controls. <br>

**Preconditions:** Admin user must be logged in. Active tickets must exist in the system.

**Scenario 1: Call Next Customer**

| #   | Step                                              | Expected Behavior                                                                                                                                       |
| --- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | In the sidebar, tap `Queue Management` menu item. | Verify that the `Queue Management` screen is shown.                                                                                                     |
| 2   | Observe the `Queue Controls` section.             | Verify that the `Call Next` button is visible.                                                                                                          |
| 3   | Tap the `Call Next` button.                       | Verify that the system updates the `Serving` card with the next ticket number and the ticket's status in the `Current Queue` list changes to "Serving". |

**Scenario 2: Complete Service**

| #   | Step                                                                         | Expected Behavior                                                                                                 |
| --- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| 1   | While a ticket is currently being served, tap the `Complete Service` button. | Verify that the currently serving ticket is marked as completed and removed from the active `Current Queue` list. |
| 2   | Observe the dashboard cards.                                                 | Verify that the `Completed Services` count increases and `Current Queue Length` updates accurately.               |

**Scenario 3: Skip Ticket**

| #   | Step                                                                                             | Expected Behavior                                                                                            |
| --- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| 1   | While a ticket is currently being served (or if a customer is a no-show), tap the `Skip` button. | Verify that the current ticket is flagged as skipped.                                                        |
| 2   | Observe the `Serving` and `Next in Queue` cards.                                                 | Verify that the system automatically calls the next ticket in line and updates the respective display cards. |

**Post-conditions:**

- The queue state successfully updates in real-time according to the admin's queue control actions.
