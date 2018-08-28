---
swagger: "2.0"
x-collection-name: PayJunction
x-complete: 0
info:
  title: PayJunction Delete Transactions Notes
  description: /transactions/{transactionid}/notes/{noteid}.
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /customers/{customerId}/notes:
    get:
      summary: Get Customers Notes
      description: /customers/{customerid}/notes.
      operationId: CustomersNotesByCustomerIdGet
      x-api-path-slug: customerscustomeridnotes-get
      parameters:
      - in: path
        name: customerId
      - in: query
        name: limit
      - in: query
        name: offset
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Notes
    post:
      summary: Post Customers Notes
      description: /customers/{customerid}/notes.
      operationId: CustomersNotesByCustomerIdPost
      x-api-path-slug: customerscustomeridnotes-post
      parameters:
      - in: path
        name: customerId
      - in: formData
        name: note
        description: Max Length 2048
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Notes
  /customers/{customerId}/notes/{noteId}:
    get:
      summary: Get Customers Notes
      description: /customers/{customerid}/notes/{noteid}.
      operationId: CustomersNotesByCustomerIdAndNoteIdGet
      x-api-path-slug: customerscustomeridnotesnoteid-get
      parameters:
      - in: path
        name: customerId
      - in: path
        name: noteId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Notes
    put:
      summary: Put Customers Notes
      description: /customers/{customerid}/notes/{noteid}.
      operationId: CustomersNotesByCustomerIdAndNoteIdPut
      x-api-path-slug: customerscustomeridnotesnoteid-put
      parameters:
      - in: header
        name: Content-Type
      - in: path
        name: customerId
      - in: formData
        name: note
        description: Max Length 2048
      - in: path
        name: noteId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Notes
    delete:
      summary: Delete Customers Notes
      description: /customers/{customerid}/notes/{noteid}.
      operationId: CustomersNotesByCustomerIdAndNoteIdDelete
      x-api-path-slug: customerscustomeridnotesnoteid-delete
      parameters:
      - in: path
        name: customerId
      - in: path
        name: noteId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Customers
      - Notes
  /transactions/{transactionId}/notes:
    get:
      summary: Get Transactions Notes
      description: Get a list of notes for a transaction
      operationId: TransactionsNotesByTransactionIdGet
      x-api-path-slug: transactionstransactionidnotes-get
      parameters:
      - in: query
        name: limit
      - in: query
        name: offset
      - in: path
        name: transactionId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Transactions
      - Notes
    post:
      summary: Post Transactions Notes
      description: /transactions/{transactionid}/notes/.
      operationId: TransactionsNotesByTransactionIdPost
      x-api-path-slug: transactionstransactionidnotes-post
      parameters:
      - in: formData
        name: note
      - in: path
        name: transactionId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Transactions
      - Notes
  /transactions/{transactionId}/notes/{noteId}:
    get:
      summary: Get Transactions Notes
      description: /transactions/{transactionid}/notes/{noteid}.
      operationId: TransactionsNotesByTransactionIdAndNoteIdGet
      x-api-path-slug: transactionstransactionidnotesnoteid-get
      parameters:
      - in: path
        name: noteId
      - in: path
        name: transactionId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Transactions
      - Notes
    put:
      summary: Put Transactions Notes
      description: /transactions/{transactionid}/notes/{noteid}.
      operationId: TransactionsNotesByTransactionIdAndNoteIdPut
      x-api-path-slug: transactionstransactionidnotesnoteid-put
      parameters:
      - in: formData
        name: note
      - in: path
        name: noteId
      - in: path
        name: transactionId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Transactions
      - Notes
    delete:
      summary: Delete Transactions Notes
      description: /transactions/{transactionid}/notes/{noteid}.
      operationId: TransactionsNotesByTransactionIdAndNoteIdDelete
      x-api-path-slug: transactionstransactionidnotesnoteid-delete
      parameters:
      - in: path
        name: noteId
      - in: path
        name: transactionId
      - in: header
        name: X-PJ-Application-Key
      responses:
        200:
          description: OK
      tags:
      - Transactions
      - Notes
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