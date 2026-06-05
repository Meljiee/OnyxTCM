## **SEC-0004:** Security testing - Admin Route Protection
> **Summary:** Verify that a standard student user cannot bypass role-based access control to view admin-only routes. <br>

**Preconditions:** User is logged in with a standard "Student" role. 

**Scenario 1: Attempt Forced Navigation**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Ensure the user is currently on the `Not in a Queue yet?` dashboard (`/home`). | Verify standard user access. |
| 2 | Click on the browser's URL address bar. | The current URL is highlighted. |
| 3 | Manually type the admin dashboard route (e.g., `/dashboard` or `/queue-management`) and press `Enter`. | Verify the system attempts to route the user. |
| 4 | Observe the resulting screen. | Verify that the application middleware intercepts the request and either displays a `403 Forbidden` error or immediately redirects the user back to the `/home` screen. |

**Post-conditions:**
- The standard user remains restricted from accessing administrative interfaces and data.