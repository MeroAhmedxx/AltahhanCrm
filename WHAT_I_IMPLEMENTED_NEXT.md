# WHAT I IMPLEMENTED NEXT

## Pro workflow upgrades

### 1) Client-specific price memory
- Added `deal_client_prices` table.
- Every time a deal item is added or updated, the system remembers the client's last price for that product.
- When adding a new item row, leaving unit price empty now auto-pulls the saved client price when available.
- Initial deal creation also reuses remembered client pricing if unit price is left blank.

### 2) Editable structured deal items
- Added inline update route for shipment deal items.
- Added delete route for shipment deal items.
- Deal page now supports item editing without leaving the workflow.
- Recalculation and validation run again after every item change.

### 3) Better Documents Center
- Unified `/documents` now includes:
  - shipment documents
  - generated deal export packs from `deal_documents`
  - client invoices
  - entity attachments
- Added KPI cards.
- Added source filter.
- Added open-source link and correct file links for generated export docs.

### 4) UX polish for deal workflow
- Deal page now uses editable item cards instead of a read-only table.
- Added client pricebook panel.
- Better mobile layout for actions and item editing.

## Validation
- `python -m py_compile app.py` passed successfully.
