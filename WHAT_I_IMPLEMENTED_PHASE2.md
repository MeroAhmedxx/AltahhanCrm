Phase 2 patch summary

Implemented now:
- Added deal_payments table creation in app startup.
- Added payment helpers to calculate:
  - paid amount
  - remaining amount
  - payment status (Paid / Partial / Unpaid / Overdue / Draft)
  - paid percentage
- Added POST route: /deal/{deal_id}/payment/add
- Upgraded deal detail page with:
  - payment KPIs
  - add payment form
  - payments history table
- Upgraded shipment detail page with:
  - shipment finance snapshot
  - per-deal paid/remaining/payment status columns
- Upgraded deals index page with payment visibility.
- Upgraded reports page with:
  - collection snapshot
  - client finance table
  - payment book
  - shipment finance table
- Upgraded reports export Excel with sheets:
  - Summary
  - Team
  - Payments
  - Shipment Finance
- Added python-docx to requirements for current document generation code.

Notes:
- This patch extends the existing shipment-centric architecture without moving logic out of app.py yet.
- No destructive schema migration was used; missing tables are created automatically at startup.
