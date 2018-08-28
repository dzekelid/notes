---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay Create and Update Customer
  description: |-
    Create a customer in ARC using the following attributes (at minimum by providing values for required attributes). If providing an identifier for an existing customer, its information is updated.<br><br>
    *Note: Any additional non-standard attribute will be stored with customer record and available for presentment rendering.*
  contact:
    name: VersaPay Support
    url: https://www.versapay.com/support
    email: support@versapay.com
  version: 1.0.0
host: secure.versapay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/imports/payment:
    post:
      summary: Create a Payment
      description: |-
        Create and update external payment records in ARC.<br><br>The set of attributes to send in the request body may vary based on the account configuration. Please contact the implementation specialist for more information.<br><br>
        The request schema for posting a payment for a single invoice is slightly different than that for posting a payment for multiple invoices.

        For instance, sample request for posting payment for a single invoice looks like:
        ```
        {
          "identifier": "PMT0010-05",
          "invoice_number": "INV1234-01",
          "amount": 10000,
          "currency": "usd",
          "date": "2018-01-10",
          "customer_identifier": "C1234",
          "customer_name": "Acme Inc.",
          "notes": "Notes",
          "ref1": "1234",
          "ref2": "PO# 84767"
        }
        ```

        *Note: Customer will be created using the customer_&ast; attributes if it doesn???t already exist at the time of payment import.*
      operationId: createPayment
      x-api-path-slug: apiimportspayment-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - CreatePayment
  /api/imports/customer:
    post:
      summary: Create and Update Customer
      description: |-
        Create a customer in ARC using the following attributes (at minimum by providing values for required attributes). If providing an identifier for an existing customer, its information is updated.<br><br>
        *Note: Any additional non-standard attribute will be stored with customer record and available for presentment rendering.*
      operationId: createCustomer
      x-api-path-slug: apiimportscustomer-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
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