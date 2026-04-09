# What I Implemented Now - Automation Patch

## Core upgrades
- Added `shipment_deal_items` table for structured product rows per customer deal.
- Added automatic roll-up from deal items into:
  - product summary
  - qty ton
  - cartons
  - net/gross weights
  - total amount
- Added smart validation before document generation.
- Upgraded document generation to use structured item data.
- Added batch action on shipment page:
  - **Generate Full Export Pack** for all deals in the shipment.
- Saved shipment-level batch zip into shipment documents.

## New routes
- `POST /deal/{deal_id}/item/add`
- `POST /shipment/{shipment_id}/generate-all-packs`

## UI upgrades
- Deal page now shows:
  - validation board
  - structured shipment items table
  - add product row form from catalog
- Shipment page now shows:
  - Generate Full Export Pack button
  - success / warning / error banners
  - open link for generated shipment export batch

## Notes
- Existing deal creation still works, but now also seeds the first structured item row automatically when product data is provided.
- `app.py` passed `python -m py_compile` after the patch.
