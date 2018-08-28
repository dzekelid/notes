---
swagger: "2.0"
x-collection-name: NxtPort
x-complete: 0
info:
  title: NxtPort T-mining Secure Container Release API Record delivery
  description: When the driver has delivered the container, a request should be sent
    to the server to record (create) the delivery. Note that a delivery is associated
    with a PickupRight, because the driver who gets a PickupRight, will automatically
    get a right to deliver the container. For that reason, the PickupRight must be
    reported.
  contact:
    name: T-Mining API support
    url: http://support.t-mining.be/
    email: support@t-mining.be
  version: 1.0.0
host: api.nxtport.eu
basePath: /blockchain
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/deliveries:
    post:
      summary: Record delivery
      description: When the driver has delivered the container, a request should be
        sent to the server to record (create) the delivery. Note that a delivery is
        associated with a PickupRight, because the driver who gets a PickupRight,
        will automatically get a right to deliver the container. For that reason,
        the PickupRight must be reported.
      operationId: postApiV1Deliveries
      x-api-path-slug: apiv1deliveries-post
      parameters:
      - in: query
        name: api_token
        description: authentication token of user making the request
      responses:
        2:
          description: Successful response
        200:
          description: OK
      tags:
      - Record
      - Delivery
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