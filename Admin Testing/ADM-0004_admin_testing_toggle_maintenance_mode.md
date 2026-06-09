## **ADM-0004:** Admin testing - Toggle Maintenance Mode

> **Summary:** Verify that the admin can toggle the system maintenance mode in General Settings. <br>

**Preconditions:** Admin user must be logged in.

**Scenario 1**

| #   | Step                                                   | Expected Behavior                                                                    |
| --- | ------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| 1   | In the sidebar, tap `Settings` menu item.              | Verify that the `Systems Settings` screen is shown, defaulting to the `General` tab. |
| 2   | Observe the `General Settings` section.                | Verify that the `Maintenance Mode` toggle switch is visible.                         |
| 3   | Tap the `Maintenance Mode` toggle switch to enable it. | Verify that the toggle switch turns on.                                              |
| 4   | Tap the `Save Changes` button.                         | Verify that the system state updates and saves the setting.                          |

**Post-conditions:**

- The system is placed into or taken out of maintenance mode.
