Altahhan repo focused fix bundle

This bundle is meant to be copied over the GitHub repo:
MeroAhmedxx/AltahhanCrm

Included:
- templates/shipment_detail.html
  - dark contrast fix
  - no white alert cards
  - client autofill script using the existing /current-client/{id} page
- templates/deal_detail.html
  - dark contrast fix
  - structured items editing section
  - payments section clearer
- templates/shipments.html
  - dark contrast fix
- data/document_templates/invoice_packing_template.xlsm
  - replaced with the real invoice workbook uploaded by the user
- data/document_templates/cad_template.docx
  - replaced with the real CAD template uploaded by the user
- data/document_templates/Packing List REAL REFERENCE.pdf
  - reference file for matching output formatting

Important:
- This bundle does not replace app.py.
- Autofill is implemented client-side by reading the existing current-client page.
- After replacing the files, redeploy and hard refresh the browser.
