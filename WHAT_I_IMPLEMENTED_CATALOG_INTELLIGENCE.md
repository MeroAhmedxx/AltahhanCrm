Phase 5 - Catalog Intelligence

Implemented on top of Altahhan Edition:

1. Structured product catalog upgrade
- Expanded export_products to support:
  - product_line
  - sku
  - weight_label
  - pack_size
  - flavor
  - presentation
  - brochure_page
- Added automatic migration for existing databases.

2. Altahhan brochure data seeding
- Rebuilt data/export_catalog.json with a richer Altahhan product set derived from the catalog pages.
- Added POST /export/products/seed-altahhan to sync brochure data into the live database.
- Added /catalog as a direct browser route for the catalog UI.

3. Pro catalog UI
- Replaced the old export_products page with a searchable grouped catalog browser.
- Added category filters, KPI cards, brochure sync action, and richer product metadata cards.

4. Shipment integration
- Added product presets into shipment deal creation using a datalist sourced from export_products.
- This helps teams use consistent product names and weights while creating customer deals.

5. API helper
- Added /export/products/suggest for lightweight product lookup / autocomplete-ready JSON.

Validation
- app.py passes python -m py_compile.
