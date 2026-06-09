# SEC-0005: Security Testing - Session Logout Destruction

## Summary

Verify that triggering a logout request opens a confirmation mechanism, completely destroys all active session tokens upon acceptance, and securely redirects the client back to the production deployment login route.

**Preconditions:**

- The target user is actively logged into their respective module dashboard with a live session handshake token.

---

**Scenario 1: Student / Standard User Logout**

| #   | Step                                                                              | Expected Behavior                                                                                                                                     |
| --- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Verify that you are currently logged in and on the customer tracking layout view. | Active ticket details or queue positions are visible.                                                                                                 |
| 2   | Tap the `Log Out` button located on the customer navigation panel bar.            | Verify that a confirmation modal or browser alert appears asking to confirm the sign-out request.                                                     |
| 3   | Click the `Logout` button on the modal pop-up interface.                          | Verify that the client browser wipes the stored active session token from local storage immediately.                                                  |
| 4   | Wait for the interface redirection to finish.                                     | Verify that the user is instantly redirected to the production environment route: `https://queuely-one.vercel.app/login`.                             |
| 5   | Click on the web browser's native "Back" navigation arrow button.                 | Verify that the browser does not re-authenticate the user; the system must remain locked on the login page, blocking access to private customer data. |

---

**Scenario 2: Admin / Staff Session Termination**

| #   | Step                                                                                                                                  | Expected Behavior                                                                                                                                          |
| --- | ------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Verify that you are logged in with administrative access on the private Admin Dashboard panel.                                        | Live system monitoring data and queue configurations are displayed.                                                                                        |
| 2   | Click on the administrative logout control switch component.                                                                          | Verify that a confirmation modal layer prompts the operator to verify their intent to terminate the session.                                               |
| 3   | Click the `Logout` button on the confirmation module window.                                                                          | The application drops the WebSocket connection pool and invalidates the session token within Supabase Auth.                                                |
| 4   | Wait for the interface network routing steps to finish.                                                                               | Verify the client is instantly moved back to the production deployment URL: `https://queuely-one.vercel.app/login`.                                        |
| 5   | Click the web browser's "Back" arrow button or manually type a direct local or production route link (e.g., `/admin`) in the URL bar. | Verify that application middleware interceptors catch the request, block access, reject raw database queries, and force the user back to the sign-in menu. |

**Post-conditions:**

- All high-privilege access permissions are revoked, and the client is safely isolated at the production login checkpoint interface.
