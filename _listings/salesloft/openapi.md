swagger: "2.0"
x-collection-name: SalesLoft
x-complete: 1
info:
  title: SalesLoft
  description: salesloft-helps-transform-sales-teams-into-modern-sales-organizations---converting-more-target-accounts-into-customer-accounts
  version: v2
host: api.salesloft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/notes.json:
    get:
      summary: List notes
      description: |-
        Fetches multiple note records. The records can be filtered, paged, and sorted according to
        the respective parameters.
      operationId: v2.notes.json.get
      x-api-path-slug: v2notes-json-get
      parameters:
      - in: query
        name: associated_with_id
        description: ID of the item with which the note is associated
      - in: query
        name: associated_with_type
        description: Case insensitive type of item with which the note is associated
      - in: query
        name: ids
        description: IDs of notes to fetch
      - in: query
        name: include_paging_counts
        description: Whether to include total_pages and total_count in the metadata
      - in: query
        name: page
        description: The current page to fetch results from
      - in: query
        name: per_page
        description: How many records to show per page in the range [1, 100]
      - in: query
        name: sort_by
        description: 'Key to sort on, must be one of: created_at, updated_at'
      - in: query
        name: sort_direction
        description: 'Direction to sort in, must be one of: ASC, DESC'
      - in: query
        name: updated_at
        description: Equality filters that are applied to the updated_at field
      responses:
        200:
          description: OK
      tags:
      - Sales
      - List
      - Notes
    post:
      summary: Create a note
      description: Creates a note.
      operationId: v2.notes.json.post
      x-api-path-slug: v2notes-json-post
      parameters:
      - in: formData
        name: associated_with_id
        description: ID of the item with which the note is associated
      - in: formData
        name: associated_with_type
        description: Case insensitive type of item with which the note is associated
      - in: formData
        name: call_id
        description: ID of the call with which the note is associated
      - in: formData
        name: content
        description: The content of the note
      - in: formData
        name: skip_crm_sync
        description: Boolean indicating if the CRM sync should be skipped
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Note
  /v2/notes/{id}.json:
    get:
      summary: Fetch a note
      description: Fetches a note, by ID only.
      operationId: v2.notes.id.json.get
      x-api-path-slug: v2notesid-json-get
      parameters:
      - in: path
        name: id
        description: Note ID
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Fetch
      - Note
    put:
      summary: Update a note
      description: Updates a note. Any changes to the note or associated records will
        not reflect in Salesforce.com.
      operationId: v2.notes.id.json.put
      x-api-path-slug: v2notesid-json-put
      parameters:
      - in: formData
        name: call_id
        description: ID of the call with which the note is associated
      - in: formData
        name: content
        description: The content of the note
      - in: path
        name: id
        description: Note ID
      responses:
        200:
          description: OK
      tags:
      - Sales
      - Note