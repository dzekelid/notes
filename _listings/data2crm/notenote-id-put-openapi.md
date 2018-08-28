---
swagger: "2.0"
x-collection-name: Data2CRM
x-complete: 0
info:
  title: Data2CRM PUT for Note
  description: Update note information
  version: "1"
host: api.data2crm.com:80
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /note/{note_id}:
    delete:
      summary: DELETE for Note
      description: Delete note information
      operationId: deleteNoteEntity
      x-api-path-slug: notenote-id-delete
      parameters:
      - in: path
        name: note_id
        description: Note Identifier
      - in: header
        name: X-API2CRM-CRMKEY
        description: CRM Key
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - Notes
    get:
      summary: GET for Note
      description: Return note information
      operationId: getNoteEntity
      x-api-path-slug: notenote-id-get
      parameters:
      - in: path
        name: note_id
        description: Note Identifier
      - in: header
        name: X-API2CRM-CRMKEY
        description: CRM Key
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - Notes
    put:
      summary: PUT for Note
      description: Update note information
      operationId: updateNoteEntity
      x-api-path-slug: notenote-id-put
      parameters:
      - in: body
        name: body
        description: Update note information
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: note_id
        description: Note Identifier
      - in: header
        name: X-API2CRM-CRMKEY
        description: CRM Key
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
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