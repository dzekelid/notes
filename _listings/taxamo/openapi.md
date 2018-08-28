swagger: "2.0"
x-collection-name: Taxamo
x-complete: 1
info:
  title: Taxamo
  description: taxamos-elegant-suite-of-apis-and-comprehensive-reporting-dashboard-enables-digital-merchants-to-easily-comply-with-eu-regulatory-requirements-on-tax-calculation-evidence-collection-tax-return-creation-and-data-storage-
  version: "1"
host: api.taxamo.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/transactions/{key}/invoice/refunds/{refund_note_number}/send_email:
    post:
      summary: Email Credit Note
      description: Email credit note.
      operationId: emailRefund
      x-api-path-slug: apiv1transactionskeyinvoicerefundsrefund-note-numbersend-email-post
      parameters:
      - in: body
        name: input
        description: Input
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: key
        description: Transaction key
      - in: path
        name: refund_note_number
        description: Refund note id
      responses:
        200:
          description: OK
      tags:
      - Email
      - Credit
      - Note