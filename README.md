# FacilityFlow — Laboratory 4, Section B (GitHub-only)

This version runs as a static website using **HTML, CSS, JavaScript, GitHub Pages, and browser localStorage**. It does not use Supabase, a database server, Node.js, or a backend.

## Features
- Three demo roles: Administrator, Facility Staff, Requester
- Login screen and role-based dashboard/navigation
- Facility listing and Administrator facility creation
- Reservation submission, Pending status, approval/rejection
- Reservation status flow: Pending → Scheduled → In Use → Completed
- Requester cancellation of own Pending reservation
- Start/end validation, maintenance-facility blocking, overlapping active schedule checks
- Service request submission
- Audit trail for reservation and facility actions
- User role listing and responsive interface

## Demo login accounts
| Role | Username | Password |
|---|---|---|
| Administrator | `admin` | `admin123` |
| Facility Staff | `staff` | `staff123` |
| Requester | `requester` | `requester123` |

Change these demo credentials in `js/app.js` before sharing a public demonstration.

## Run locally
Open `index.html` in a browser. No installation or Node.js is required.

## Publish using GitHub Pages
1. Create a new GitHub repository.
2. Upload the contents of this folder. `index.html` must be at the repository root.
3. Open repository **Settings → Pages**.
4. Under Build and deployment, select **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then Save.
6. Wait for deployment and open the Pages URL shown by GitHub.

## Important limitation: GitHub-only mode
GitHub Pages is static hosting. This implementation simulates login and role permissions in browser JavaScript and stores records in the visitor's browser localStorage. It is suitable as a classroom prototype/demo, but it is **not secure authentication or centralized multi-user storage**. Users can inspect or alter browser data, and different browsers/devices do not share records. A real organizational system requires a trusted backend and server-side authorization. Do not use real personal or confidential data.

## Reset demo data
Open browser developer tools → Console and run:
```js
localStorage.removeItem("facilityflow_github_demo_v1");
location.reload();
```
The initial demo accounts and sample facilities will be restored.
