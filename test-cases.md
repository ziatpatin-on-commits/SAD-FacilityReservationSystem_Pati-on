# Functional Test Checklist

| Test ID | Scenario | Expected result |
|---|---|---|
| TC-B4-01 | Requester submits reservation | Saved as Pending |
| TC-B4-02 | Submit overlapping scheduled time | Conflict detected and blocked |
| TC-B4-03 | Administrator approves request | Status becomes Scheduled |
| TC-B4-04 | Administrator rejects request | Status becomes Rejected |
| TC-B4-05 | Staff marks facility In Use | Status updated |
| TC-B4-06 | Staff completes reservation | Status becomes Completed |
| TC-B4-07 | Requester attempts to act on another user's request | No action is provided in the interface |
| TC-B4-08 | Reserve facility under Maintenance | Blocked |
| TC-B4-09 | Check audit log | Admin can view logged actions |
| TC-B4-10 | Open protected page without login | App initially shows login screen |

Record actual results and screenshots after testing. Note: this static GitHub Pages prototype has client-side-only role checks; it cannot provide secure access control.
