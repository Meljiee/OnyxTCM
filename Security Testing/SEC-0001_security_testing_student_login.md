# SEC-0001: Security Testing - Student and Admin Login

## Summary

Verify that users can successfully log in using the unified Queuely single log-in interface, and that the system safely rejects invalid password vectors.

**Preconditions:** - The target user account (Student or Admin/Staff) must already be provisioned in the database schema.

- The user must currently be completely logged out.

---

## Scenario 1: Standard Student Login (Valid Credentials)

| #   | Step                                                                      | Expected Behavior                                                                                                                              |
| --- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Launch the Queuely web application URL.                                   | Verify that the `Welcome Back` centralized login screen is displayed.                                                                          |
| 2   | Set the `Preferred Name` text field to your name (e.g., "Ricky").         | Verify that the text field value matches the string input precisely.                                                                           |
| 3   | Enter a valid registered student email address in the `Email` text field. | Verify that the input is accepted without validation errors.                                                                                   |
| 4   | Enter the correct password in the `Password` text field.                  | Verify that the input character string is securely masked.                                                                                     |
| 5   | Tap the `Sign In` button.                                                 | Verify that the application forwards the session handshake payload to the Supabase Auth API.                                                   |
| 6   | Wait until the background loading cycle completes.                        | Verify that the student is routed to the `Not in a Queue yet?` dashboard (`/home`), displaying a personalized greeting (e.g., "Hello, Ricky"). |

**Post-conditions:**

- The Student is authenticated, and a secure active session token is established in browser storage.

---

## Scenario 2: Standard Student Login (Invalid Password)

| #   | Step                                                                    | Expected Behavior                                                                                                                                               |
| --- | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Launch the Queuely login screen interface.                              | Verify that the baseline log-in fields are cleanly loaded.                                                                                                      |
| 2   | Enter an active, registered student email address in the `Email` field. | The email input is accepted.                                                                                                                                    |
| 3   | Enter an incorrect, arbitrary password string in the `Password` field.  | The password input characters are masked.                                                                                                                       |
| 4   | Tap the `Sign In` button.                                               | Verify that the Supabase Auth module rejects the credentials.                                                                                                   |
| 5   | Observe the resulting client screen layout.                             | Verify that a secure error message ("Invalid login credentials") is displayed, no session tokens are generated, and the user remains locked on the log-in page. |

---

## Scenario 3: Admin / Staff Login (Valid Credentials)

| #   | Step                                                                        | Expected Behavior                                                                                                                             |
| --- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | Open the centralized single log-in window.                                  | Verify that the system layout renders the core authentication text fields.                                                                    |
| 2   | Enter a valid, registered administrator email address in the `Email` field. | Input value is accepted.                                                                                                                      |
| 3   | Enter the correct matching password string in the `Password` field.         | Verify the input string values are completely masked.                                                                                         |
| 4   | Tap the `Sign In` button.                                                   | The system processes user verification rules.                                                                                                 |
| 5   | Wait for database role-validation mapping to complete.                      | Verify that the application maps the user's metadata role and automatically routes them directly to the private Admin Dashboard layout panel. |

**Post-conditions:**

- High-privilege administrative backend access is granted; session parameters match an active admin role state.

---

## Scenario 4: Admin / Staff Login (Invalid Password)

| #   | Step                                                                   | Expected Behavior                                                                                                                                                  |
| --- | ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | Open the main login console.                                           | The login components load correctly.                                                                                                                               |
| 2   | Enter a valid administrative email address in the `Email` field.       | Input value is captured.                                                                                                                                           |
| 3   | Input an invalid or corrupted password string in the `Password` field. | Characters are securely masked.                                                                                                                                    |
| 4   | Tap the `Sign In` button.                                              | The backend database triggers an authentication rejection error.                                                                                                   |
| 5   | Observe the resulting console screen.                                  | Verify that administrative access is blocked, a generic login failure notification is shown, and the user is prevented from viewing any protected directory trees. |
