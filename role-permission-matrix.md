# Role-Permission Matrix

| Function | Administrator | Facility Staff | Requester |
|---|---|---|---|
| View facilities | Yes | Yes | Yes |
| Add facilities | Yes | No | No |
| Submit reservation | Yes | Yes | Yes |
| View reservations | All | All | Own only |
| Approve/reject | Yes | No | No |
| Mark In Use / Completed | Yes | Yes | No |
| Cancel own Pending reservation | Yes | Yes | Yes |
| Submit service request | Yes | Yes | Yes |
| View service requests | All | All | Own only |
| View audit logs | Yes | No | No |

## Reservation workflow
`Submitted → Pending → Administrator Review → Rejected`
or
`Submitted → Pending → Administrator Review → Scheduled → In Use → Completed`

## Business rules
- BR-B4-01: Only active facilities may be reserved.
- BR-B4-02: Reservation start must precede end time.
- BR-B4-03: Overlapping Scheduled/In Use schedules are blocked by the browser application.
- BR-B4-04: Only Administrator can approve or reject.
- BR-B4-05: Rejected reservations cannot be scheduled.
- BR-B4-06: Scheduled reservations hold the time slot.
- BR-B4-07: Completed reservations have no edit action in the UI.
- BR-B4-08: Maintenance facilities cannot be reserved.
- BR-B4-09: Requesters can cancel only their own Pending requests.
- BR-B4-10: Reservation and facility actions are written to the local audit log.
