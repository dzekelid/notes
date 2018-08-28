---
swagger: "2.0"
x-collection-name: Data2CRM
x-complete: 0
info:
  title: Data2CRM POST for Note
  description: Add note into the system
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
  /note:
    get:
      summary: GET for Note
      description: Returns all notes from the system
      operationId: getNoteCollection
      x-api-path-slug: note-get
      parameters:
      - in: query
        name: filter
        description: Filter
      - in: query
        name: limit
        description: 'Amount of results (default: 25)'
      - in: query
        name: offset
        description: 'Start from record (default: 0)'
      - in: query
        name: parent_id
        description: Parent Identifier
      - in: query
        name: parent_type
        description: Parent Type
      - in: header
        name: X-API2CRM-CRMKEY
        description: CRM Key
      - in: header
        name: X-API2CRM-DATA-ENABLE
        description: Data Enable
      - in: header
        name: X-API2CRM-USERKEY
        description: User Key
      responses:
        200:
          description: OK
      tags:
      - Note
    post:
      summary: POST for Note
      description: Add note into the system
      operationId: createNoteEntity
      x-api-path-slug: note-post
      parameters:
      - in: body
        name: body
        description: Add note into the system
        schema:
          $ref: '#/definitions/holder'
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
      - Note
  /note/count:
    get:
      summary: COUNT for Note
      description: Count all notes from the system
      operationId: getNoteCountCollection
      x-api-path-slug: notecount-get
      parameters:
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
      - Note
      - Count
  /note/describe:
    get:
      summary: DESCRIBE for Note
      description: Returns describe for notes
      operationId: getNoteDescribe
      x-api-path-slug: notedescribe-get
      parameters:
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
      - Note
      - Describe
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