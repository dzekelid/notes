---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Photos Notes Edit
  description: Edit a note on a photo. Coordinates and sizes are in pixels, based
    on the 500px image size shown on individual photo pages.
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.photos.notes.add:
    post:
      summary: Photos Notes Add
      description: Add a note to a photo. Coordinates and sizes are in pixels, based
        on the 500px image size shown on individual photo pages.
      operationId: postRestMethodFlickr.photos.notes.add
      x-api-path-slug: restmethodflickr-photos-notes-add-post
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: note_h
        description: The height of the note
      - in: query
        name: note_text
        description: The description of the note
      - in: query
        name: note_w
        description: The width of the note
      - in: query
        name: note_x
        description: The left coordinate of the note
      - in: query
        name: note_y
        description: The top coordinate of the note
      - in: query
        name: photo_id
        description: The id of the photo to add a note to
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Notes
      - Add
  /rest/?method=flickr.photos.notes.delete:
    post:
      summary: Photos Notes Delete
      description: Delete a note from a photo.
      operationId: postRestMethodFlickr.photos.notes.delete
      x-api-path-slug: restmethodflickr-photos-notes-delete-post
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: note_id
        description: The id of the note to delete
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Notes
      - Delete
  /rest/?method=flickr.photos.notes.edit:
    post:
      summary: Photos Notes Edit
      description: Edit a note on a photo. Coordinates and sizes are in pixels, based
        on the 500px image size shown on individual photo pages.
      operationId: postRestMethodFlickr.photos.notes.edit
      x-api-path-slug: restmethodflickr-photos-notes-edit-post
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: note_h
        description: The height of the note
      - in: query
        name: note_id
        description: The id of the note to edit
      - in: query
        name: note_text
        description: The description of the note
      - in: query
        name: note_w
        description: The width of the note
      - in: query
        name: note_x
        description: The left coordinate of the note
      - in: query
        name: note_y
        description: The top coordinate of the note
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Notes
      - Edit
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