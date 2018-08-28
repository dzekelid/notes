---
swagger: "2.0"
x-collection-name: Click Meter
x-complete: 0
info:
  title: Click Meter Fast patch the "notes" field of a group
  description: Fast patch the "notes" field of a group.
  contact:
    name: Api Support
    url: http://www.clickmeter.com/api
    email: api@clickmeter.com
  version: v2
host: apiv2.clickmeter.com:80
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /conversions/{conversionId}/notes:
    put:
      summary: Fast patch the "notes" field of a conversion
      description: Fast patch the "notes" field of a conversion.
      operationId: putConversionsConversionNotes
      x-api-path-slug: conversionsconversionidnotes-put
      parameters:
      - in: path
        name: conversionId
        description: Id of the conversion
      - in: body
        name: note
        description: Patch requests
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Conversions
      - ConversionId
      - Notes
  /datapoints/{id}/notes:
    put:
      summary: Fast patch the "notes" field of a datapoint
      description: Fast patch the "notes" field of a datapoint.
      operationId: putDatapointsNotes
      x-api-path-slug: datapointsidnotes-put
      parameters:
      - in: path
        name: id
        description: Id of the datapoint
      - in: body
        name: note
        description: Patch requests
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Datapoints
      - Id
      - Notes
  /groups/{id}/notes:
    put:
      summary: Fast patch the "notes" field of a group
      description: Fast patch the "notes" field of a group.
      operationId: putGroupsNotes
      x-api-path-slug: groupsidnotes-put
      parameters:
      - in: path
        name: id
        description: Id of the group
      - in: body
        name: note
        description: Patch requests
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Groups
      - Id
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