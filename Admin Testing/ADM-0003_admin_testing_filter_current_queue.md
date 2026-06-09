## **ADM-0003:** Admin testing - Filter Current Queue

> **Summary:** Verify that the admin can search and filter the current queue list by ticket number. <br>

**Preconditions:** Admin user must be logged in. Active tickets must exist in the queue.

**Scenario 1**

| #   | Step                                                                                | Expected Behavior                                                                        |
| --- | ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| 1   | Navigate to the `Queue Management` screen.                                          | Verify that the `Search Queue` text field is visible.                                    |
| 2   | Enter a valid ticket number (e.g., "12") in the `Filter By Ticket Queue` textfield. | Verify that the `Current Queue` list filters to display only the matching ticket row(s). |

**Post-conditions:**

- The admin successfully locates a specific ticket in the queue.
