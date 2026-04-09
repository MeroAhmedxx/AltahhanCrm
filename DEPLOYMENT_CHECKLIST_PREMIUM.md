# Deployment Checklist - Premium Release

## Before upload
- [ ] Confirm Python version from `runtime.txt`
- [ ] Confirm `requirements.txt` installs cleanly
- [ ] Confirm `CRM_DB_URL` is ready
- [ ] Confirm upload/storage path permissions

## Render setup
- [ ] Build command: `pip install -r requirements.txt`
- [ ] Start command: `gunicorn -k uvicorn.workers.UvicornWorker -w 2 -b 0.0.0.0:$PORT app:app`
- [ ] Health check path: `/login`
- [ ] Add environment variables from `render.yaml`

## Production smoke test
- [ ] Login works
- [ ] Dashboard loads
- [ ] Notifications dropdown loads
- [ ] Shipments list loads
- [ ] Shipment detail loads
- [ ] Deal detail loads
- [ ] Product catalog page loads
- [ ] Reports page loads
- [ ] Excel export works
- [ ] Full export pack generation works
- [ ] Payment entry works

## After launch
- [ ] Create one real shipment
- [ ] Add one deal and one payment
- [ ] Generate one full document pack
- [ ] Verify report totals match the deal totals
