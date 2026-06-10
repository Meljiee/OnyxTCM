## **SEC-0002:** Security testing - Student Sign Up

> **Summary:** Verify that a new user can successfully register an account using a valid student email and password. <br>

**Preconditions:** The user is on the login screen and does not currently have an account in the system.

**Scenario 1: Valid Sign Up**

| #   | Step                                                                                                    | Expected Behavior                                                               |
| --- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| 1   | On the login screen, tap the `Sign Up` link.                                                            | Verify that the `Create Account` screen is shown.                               |
| 2   | Enter a valid student email address in the `Email` textfield.                                           | Verify the input is accepted without validation errors.                         |
| 3   | Enter a secure password in the `Password` textfield and confirm it in the `Confirm Password` textfield. | Verify the inputs match and are masked.                                         |
| 4   | Tap the `Register` button.                                                                              | Verify that the system processes the registration and creates the user profile. |
| 5   | Wait for the registration to complete.                                                                  | Verify that "Verify your email" message is displayed.                           |

**Post-conditions:**

- A new user account is successfully created in the database.
