---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post Note Comments
  description: Posts a comment to this note.
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
  /{user}/notes:
    get:
      summary: Get User Notes
      description: The user's notes
      operationId: getUserNotes
      x-api-path-slug: usernotes-get
      parameters:
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Notes
    post:
      summary: Post User Notes
      description: Creates a note on behalf of the user
      operationId: postUserNotes
      x-api-path-slug: usernotes-post
      parameters:
      - in: query
        name: message
        description: Note content
      - in: query
        name: subject
        description: The subject of the Note
      - in: path
        name: user
        description: Represents the ID of the user object
      responses:
        200:
          description: OK
      tags:
      - User
      - Notes
  /{note}:
    get:
      summary: Get Note
      description: A Facebook note
      operationId: getNote
      x-api-path-slug: note-get
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
  /{note}/comments:
    get:
      summary: Get Note Comments
      description: All of the comments on this note.
      operationId: getNoteComments
      x-api-path-slug: notecomments-get
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Comments
    post:
      summary: Post Note Comments
      description: Posts a comment to this note.
      operationId: postNoteComments
      x-api-path-slug: notecomments-post
      parameters:
      - in: query
        name: message
        description: Comment text
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Comments
  /{note}/likes:
    get:
      summary: Get Note Likes
      description: Users who like this note.
      operationId: getNoteLikes
      x-api-path-slug: notelikes-get
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Likes
    post:
      summary: Post Note Likes
      description: Likes this note.
      operationId: postNoteLikes
      x-api-path-slug: notelikes-post
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Likes
    delete:
      summary: Delete Note Likes
      description: Unlikes this note.
      operationId: deleteNoteLikes
      x-api-path-slug: notelikes-delete
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Likes
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