---
swagger: "2.0"
x-collection-name: BigOven
x-complete: 0
info:
  title: Big Oven recipe/100/notes
  description: Recipe/100/notes.
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