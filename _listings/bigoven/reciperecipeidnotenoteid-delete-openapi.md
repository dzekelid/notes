---
swagger: "2.0"
x-collection-name: BigOven
x-complete: 0
info:
  title: "Big Oven Delete a review\r\n                do a DELETE Http request of
    /note/{ID}"
  description: "Delete a review\r\n                do a delete http request of /note/{id}."
  termsOfService: Please see our [terms of service](http://api2.bigoven.com/web/documentation/termsofuse
  version: partner
host: api2.bigoven.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /recipe/{recipeId}/notes:
    get:
      summary: recipe/100/notes
      description: Recipe/100/notes.
      operationId: Note_GetNotes
      x-api-path-slug: reciperecipeidnotes-get
      parameters:
      - in: query
        name: pg
        description: page (int, starting from 1)
      - in: path
        name: recipeId
        description: recipeId (int)
      - in: query
        name: rpp
        description: recipeId
      responses:
        200:
          description: OK
      tags:
      - Recipes
      - Recipe
      - RecipeId
      - Notes
  /recipe/{recipeId}/note/{noteId}:
    delete:
      summary: "Delete a review\r\n                do a DELETE Http request of /note/{ID}"
      description: "Delete a review\r\n                do a delete http request of
        /note/{id}."
      operationId: Note_Delete
      x-api-path-slug: reciperecipeidnotenoteid-delete
      parameters:
      - in: path
        name: noteId
        description: noteId (int)
      - in: path
        name: recipeId
        description: recipeId (int)
      responses:
        200:
          description: OK
      tags:
      - Recipes
      - Recipe
      - RecipeId
      - Note
      - NoteId
    get:
      summary: Get a given note. Make sure you're passing authentication information
        in the header for the user who owns the note.
      description: Get a given note. make sure you're passing authentication information
        in the header for the user who owns the note..
      operationId: Note_Get
      x-api-path-slug: reciperecipeidnotenoteid-get
      parameters:
      - in: path
        name: noteId
        description: The note ID (note -- its not the RecipeID)
      - in: path
        name: recipeId
        description: recipe identifier (integer)
      responses:
        200:
          description: OK
      tags:
      - Recipes
      - Recipe
      - RecipeId
      - Note
      - NoteId
    put:
      summary: HTTP PUT (update) a Recipe note (RecipeNote).
      description: Http put (update) a recipe note (recipenote)..
      operationId: Note_Put
      x-api-path-slug: reciperecipeidnotenoteid-put
      parameters:
      - in: path
        name: noteId
      - in: path
        name: recipeId
      - in: body
        name: recipeNote
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Recipes
      - Recipe
      - RecipeId
      - Note
      - NoteId
  /recipe/{recipeId}/note:
    post:
      summary: HTTP POST a new note into the system.
      description: Http post a new note into the system..
      operationId: Note_Post
      x-api-path-slug: reciperecipeidnote-post
      parameters:
      - in: body
        name: note
        description: 'a recipe note, with fields: Date (YYYY-MM-DD string), Notes
          (string), People (string), Variations (string), RecipeID (int?)'
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: recipeId
        description: recipeId (int)
      responses:
        200:
          description: OK
      tags:
      - Recipes
      - Recipe
      - RecipeId
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