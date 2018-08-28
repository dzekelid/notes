---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post Page Notes
  description: Creates a note on the page
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{page}/notes:
    get:
      summary: Get Page Notes
      description: The notes contained on this page
      operationId: getPageNotes
      x-api-path-slug: pagenotes-get
      parameters:
      - in: path
        name: page
        description: Represents the ID of the page object
      responses:
        200:
          description: OK
      tags:
      - Page
      - Notes
    post:
      summary: Post Page Notes
      description: Creates a note on the page
      operationId: postPageNotes
      x-api-path-slug: pagenotes-post
      parameters:
      - in: query
        name: message
        description: Note content
      - in: path
        name: page
        description: Represents the ID of the page object
      - in: query
        name: subject
        description: The subject of the Note
      responses:
        200:
          description: OK
      tags:
      - Page
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