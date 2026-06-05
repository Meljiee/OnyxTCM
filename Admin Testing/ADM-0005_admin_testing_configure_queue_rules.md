## **ADM-0005:** Admin testing - Configure Queue Rules
> **Summary:** Verify that the admin can adjust automation rules like Auto-advance and Auto-rollback. <br>

**Preconditions:** Admin user must be logged in.

**Scenario 1**

| # | Step | Expected Behavior |
|---|------|-------------------|
| 1 | Navigate to the `Settings` screen. | Verify that the `Systems Settings` screen is shown. |
| 2 | Tap the `Queue Config` tab. | Verify that the `Queue Configuration` section is shown. |
| 3 | Locate the `Auto-advance Queue` setting. | Verify that the toggle switch is visible. |
| 4 | Locate the `Auto-rollback` setting. | Verify that the toggle switch is visible. |
| 5 | Toggle one or both switches. | Verify that the switches reflect the intended state (enabled/disabled). |
| 6 | Tap the `Save Changes` button. | Verify that the queue configuration updates are saved to the system. |

**Post-conditions:**
- The automated queue handling rules are updated.
