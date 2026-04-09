# Dashboard Upgrade Implemented Now

## What changed
- Rebuilt `/dashboard` into a real operations command center.
- Added finance KPIs:
  - Total Paid
  - Outstanding
  - Overdue Amount
  - Collection Rate
- Added execution KPIs:
  - Open Shipments
  - Shipments This Week
  - Tasks Due Today
  - Documents Generated (30d)
- Added collections watchlist for overdue deals.
- Added recent payments table.
- Added top clients by value.
- Kept shipment pulse, recent activity, urgent follow-ups, and hot leads.

## Files changed
- `app.py`
- `templates/dashboard.html`

## Notes
- This upgrade is safe for the current project structure and does not require a refactor first.
- The route compiles successfully with `py_compile`.
