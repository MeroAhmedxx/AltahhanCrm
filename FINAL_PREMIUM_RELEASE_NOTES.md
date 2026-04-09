# Altahhan Edition - Final Premium Release

This is the consolidated premium build of the Altahhan shipment-centric CRM / export operations platform.

## Core capabilities included
- CRM foundation: leads, pipeline, follow-ups, tasks, current clients, reminders, user management
- Shipment operations: shipments, shipment detail pages, shipment dashboard, attachments, status tracking
- Deal operations inside shipments: deal detail pages, structured line items, add/update/delete line items
- Product catalog intelligence: export products, richer product metadata, brochure-aware catalog dataset, product suggestions
- Document automation: invoice, packing list, CAD, bill generation flows, full export pack generation, ZIP bundles, document centers
- Finance and collection control: payment tracking, payment states (Draft / Paid / Partial / Unpaid / Overdue), overdue detection, finance rollups
- Reporting: payment book, client finance, shipment finance, collection snapshot, container detail, Excel export
- Dashboard: KPI command center, overdue watchlists, recent payments, top clients, shipment pulse
- Notifications: unread badge, dropdown, notifications center, due reminders
- Timeline and activity visibility: activity logs and operational traces across the workflow

## Important deployment notes
1. Set a valid `CRM_DB_URL` environment variable before first launch.
2. If you want PDF conversion from generated office documents, ensure LibreOffice is available on the host.
3. Generated files and uploads should be stored on persistent disk/storage in production.
4. Render start command is already prepared in `render.yaml`, `Procfile`, and `start.sh`.

## Recommended release steps
1. Upload this version to GitHub.
2. Create/update the production web service on Render.
3. Configure environment variables.
4. Launch once and let automatic table creation/migrations run.
5. Test these flows in order:
   - login
   - create shipment
   - create deal under shipment
   - add deal items from catalog
   - generate full export pack
   - record payment
   - open reports and export Excel

## Suggested env vars
- `CRM_DB_URL`
- `TRACKING_BASE_URL`
- `COOKIE_SECURE=true` in production
- `RENDER=true` when hosting on Render

## Final note
This bundle is intended to be a single uploadable premium release instead of incremental patches.
