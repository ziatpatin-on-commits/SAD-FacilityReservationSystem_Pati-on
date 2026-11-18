# ERD and Use Case Summary

This GitHub-only prototype stores the following logical records in browser localStorage:

- **Users**: id, username, password (demo only), name, role
- **Facilities**: id, name, location, capacity, condition, active
- **Reservations**: id, facilityId, requester, purpose, start, end, status
- **Service Requests**: id, facility, owner, category, description, status
- **Audit Logs**: id, actor, action, type, record, details, timestamp

## Relationships
- One User can submit many Reservations.
- One Facility can have many Reservations over time.
- One User can submit many Service Requests.
- One User can create many Audit Log entries.

## Use case summary
- Requester: View facilities, submit reservation, view own status/history, cancel own eligible Pending request, submit service concern.
- Facility Staff: View reservations, mark facility use, record completion, view service concerns.
- Administrator: Add/manage facilities in this demo, approve/reject reservations, view concerns, user roles and audit logs.
