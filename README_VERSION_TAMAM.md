Altahhan Version Tamam

What was verified in this build
- app.py compiles successfully
- shipment -> deal -> document generation smoke test completed successfully
- generated files in test flow:
  - invoice_packing_*.xlsm
  - invoice_packing_*.pdf
  - cad_*.docx
  - cad_*.pdf
  - document_pack_*.zip
- old databases are safer now because shipment_deal_items and deal_client_prices get in-place column upgrades on startup

Recommended real-world test after deploy
1. Open a shipment
2. Choose Existing client
3. Create deal
4. Add at least one structured item
5. Generate documents
6. Check:
   - invoice fields
   - packing fields
   - CAD
   - bill when payment method is Bill
   - zip pack

Important note
This build is aimed at being the strongest stable zip so far. Exact paragraph/cell-level wording can still be tuned further if your business templates change.
