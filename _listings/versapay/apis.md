---
name: VersaPay
x-slug: versapay
description: VersaPay handles elements of both credit and debit card merchant payment
  processing in Canada. In offering a host of merchant account services and credit
  card POS terminals it allows for an efficient merchant payment service in all aspects-
  in person, on the go, online, and at the office. Founded in 2005 by Michael Gokturk,
  VersaPay is a Canadian owned and operated national financial transaction services
  provider partnered with Chase Paymentech. Versapay also offers electronic funds
  transfer through a system called Versapay EMT.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
x-kinRank: "9"
x-alexaRank: "410909"
tags: Notes
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/versapay/apis.md
specificationVersion: "0.14"
apis:
- name: VersaPay API Reference - Create a Payment
  x-api-slug: apiimportspayment-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com//
  tags: Billing, Checking, Payments, Payments, Stack Network, Financial Services,
    Technology, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/versapay/apiimportspayment-post-openapi.md
- name: VersaPay API Reference - Create and Update Customer
  x-api-slug: apiimportscustomer-post
  description: |-
    Create a customer in ARC using the following attributes (at minimum by providing values for required attributes). If providing an identifier for an existing customer, its information is updated.<br><br>
    *Note: Any additional non-standard attribute will be stored with customer record and available for presentment rendering.*
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com//
  tags: Billing, Checking, Payments, Payments, Stack Network, Financial Services,
    Technology, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/versapay/apiimportscustomer-post-openapi.md
- name: VersaPay API Reference - Create and Update Invoice
  x-api-slug: apiimportsinvoice-post
  description: |-
    Create and update invoices in ARC. If the invoice already exists when a request is processed, it will be updated.<br><br>
    The set of attributes to send in the request body may vary based on the account configuration. Please contact the implementation specialist for more information.<br><br>
    *Note:*
      * *Customer will be created/updated using the customer_&ast; attributes if necessary at time of invoice import.*
      * *Any additional non-standard attribute will be stored with invoice record and available for presentment rendering.*
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com//
  tags: Billing, Checking, Payments, Payments, Stack Network, Financial Services,
    Technology, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/versapay/apiimportsinvoice-post-openapi.md
- name: VersaPay API Reference - Create a Payment
  x-api-slug: apiimportspayment-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com//
  tags: Billing, Checking, Payments, Payments, Stack Network, Financial Services,
    Technology, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/versapay/apiimportspayment-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://venmo.api.gallery.streamdata.io
- type: x-api-stack
  url: http://versapay.stack.network
- type: x-base
  url: https://secure.versapay.com/api/
- type: x-blog
  url: https://www.versapay.com/blog/
- type: x-blog-rss
  url: http://www.versapay.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/versapay
- type: x-crunchbase
  url: https://crunchbase.com/organization/versapay
- type: x-github
  url: https://github.com/versapay
- type: x-partners
  url: https://www.versapay.com/partners/
- type: x-support
  url: https://www.versapay.com/support/
- type: x-twitter
  url: https://twitter.com/VersaPay
- type: x-website
  url: http://developers.versapay.com/index.html
- type: x-website
  url: https://www.versapay.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---