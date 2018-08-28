---
swagger: "2.0"
x-collection-name: Google Doubleclick
x-complete: 0
info:
  title: Google Doubleclick API Insert Proposal Notes
  version: 1.0.0
  description: Add notes to the proposal
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /proposals/{proposalId}/notes:
    get:
      summary: Get Proposal Notes
      description: Get all the notes associated with a proposal
      operationId: adexchangebuyer.marketplacenotes.list
      x-api-path-slug: proposalsproposalidnotes-get
      parameters:
      - in: query
        name: pqlQuery
        description: Query string to retrieve specific notes
      - in: path
        name: proposalId
        description: The proposalId to get notes for
      responses:
        200:
          description: OK
      tags:
      - Advertising
      - Note
  /proposals/{proposalId}/notes/insert:
    post:
      summary: Insert Proposal Notes
      description: Add notes to the proposal
      operationId: adexchangebuyer.marketplacenotes.insert
      x-api-path-slug: proposalsproposalidnotesinsert-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: proposalId
        description: The proposalId to add notes for
      responses:
        200:
          description: OK
      tags:
      - Advertising
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