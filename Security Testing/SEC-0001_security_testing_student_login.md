## **SEC-0001:** Security testing - Student Login
> **Summary:** Verify that a user can successfully log in using the Queuely login screen. <br>

**Preconditions:** User account must exist in the system. The user must be logged out.

**Scenario 1**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Launch the Queuely web application. | Verify that the `Welcome Back` login screen is shown. |
| 2 | Set the `Preferred Name` textfield to your preferred name (e.g., "Ricky"). | Verify that the `Preferred Name` textfield value matches the input. |
| 3 | Set the `Email` textfield to a valid email address. | Verify that the `Email` textfield value matches the input. |
| 4 | Set the `Password` textfield to a valid password. | Verify that the `Password` textfield value is masked. |
| 5 | Tap the `Sign In` button. | Verify that the system authenticates the user. |
| 6 | Wait until loading is completed. | Verify that the `User Dashboard` (Not in a Queue yet?) screen is shown, displaying a personalized greeting (e.g., "Hello, Ricky"). |

**Post-conditions:**
- The user is authenticated and an active session is established.
