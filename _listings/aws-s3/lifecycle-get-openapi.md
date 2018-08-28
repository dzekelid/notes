---
swagger: "2.0"
x-collection-name: AWS S3
x-complete: 0
info:
  title: AWS S3 GET Bucket lifecycle
  version: 1.0.0
  description: NoteBucket lifecycle configuration now supports specifying lifecycle
    rule usingobject key name prefix, one or more object tags, or combination of both
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?lifecycle:
    get:
      summary: GET Bucket lifecycle
      description: NoteBucket lifecycle configuration now supports specifying lifecycle
        rule usingobject key name prefix, one or more object tags, or combination
        of both
      operationId: get-bucket-lifecycle
      x-api-path-slug: lifecycle-get
      responses:
        200:
          description: OK
      tags:
      - Bucket
      - Lifecycle
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