---
swagger: "2.0"
x-collection-name: Taxamo
x-complete: 0
info:
  title: Taxamo Email Credit Note
  description: Email credit note.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---