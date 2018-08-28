---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Put - to update an event note.
  version: 1.0.0
  description: Put - to update an event note..
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/todo/gettasknotes/{id}:
    get:
      summary: Get notes for a task
      description: Get notes for a task.
      operationId: DefaultToDo_GetTaskNotesByid
      x-api-path-slug: apitodogettasknotesid-get
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Notesa
      - Task
  /api/group/{id}/notes:
    get:
      summary: Get notes for Group
      description: Get notes for group.
      operationId: Group_NotesByidBypinnedBypageNumberBypageSize
      x-api-path-slug: apigroupidnotes-get
      parameters:
      - in: path
        name: id
        description: Group Id
      - in: query
        name: pageNumber
        description: Page number
      - in: query
        name: pageSize
        description: Page size
      - in: query
        name: pinned
        description: Only show pinned notes
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - NotesGroup
  /api/todo/gettodonotes:
    get:
      summary: Returns all notes for todo
      description: Returns all notes for todo.
      operationId: DefaultToDo_GetTodoNotesBytodoId
      x-api-path-slug: apitodogettodonotes-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: todoId
      responses:
        200:
          description: OK
      tags:
      - Returns
      - ""
      - Notestodo
  /api/event/{id}/addnotetoevent:
    post:
      summary: Put - to update a note on an event.
      description: Put - to update a note on an event..
      operationId: Event_AddNoteToEventByidBydataContract
      x-api-path-slug: apieventidaddnotetoevent-post
      parameters:
      - in: body
        name: dataContract
        description: the note text
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: the event id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - '-'
      - To
      - Update
      - Note
      - "On"
      - Event
  /api/event/{id}/seteventnote:
    put:
      summary: Put - to update an event note.
      description: Put - to update an event note..
      operationId: Event_UpdateEventNoteByidBynote
      x-api-path-slug: apieventidseteventnote-put
      parameters:
      - in: path
        name: id
        description: the event note id
      - in: query
        name: note
        description: the note text
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - '-'
      - To
      - Update
      - Event
      - Note
  /api/event/noteevent/add:
    post:
      summary: Adds a note to the provided role
      description: Adds a note to the provided role.
      operationId: Event_AddNoteEventByaddNoteDataContract
      x-api-path-slug: apieventnoteeventadd-post
      parameters:
      - in: body
        name: addNoteDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Note
      - To
      - Provided
      - Role
  /api/event/noteevent/unpin/{noteId}:
    post:
      summary: Unpin a Note
      description: Unpin a note.
      operationId: Event_UnpinNoteEventBynoteId
      x-api-path-slug: apieventnoteeventunpinnoteid-post
      parameters:
      - in: path
        name: noteId
        description: Id of note to unpin
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Unpin
      - Note
  /api/invoice/raisecreditnote:
    post:
      summary: Raise a credit note against invoice items on an invoice
      description: Raise a credit note against invoice items on an invoice.
      operationId: Invoice_RaiseCreditNoteBycreditNoteDataContract
      x-api-path-slug: apiinvoiceraisecreditnote-post
      parameters:
      - in: body
        name: creditNoteDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Raise
      - Credit
      - Note
      - Against
      - Invoice
      - Items
      - "On"
      - Invoice
  /api/progression/lettings/{roleId}/inventory/savenote:
    post:
      summary: Add a note to a tenant role inventory
      description: Add a note to a tenant role inventory.
      operationId: LettingsProgression_SaveInventoryNoteByroleIdBynote
      x-api-path-slug: apiprogressionlettingsroleidinventorysavenote-post
      parameters:
      - in: query
        name: note
        description: Note text
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: Tenant role id
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Tenant
      - Role
      - Inventory
  /api/offer/progressnoteofinterest:
    post:
      summary: Record a note against on a offer
      description: Record a note against on a offer.
      operationId: Offer_ProgressNoteOfInterestByofferIdBydataContract
      x-api-path-slug: apiofferprogressnoteofinterest-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: offerId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Record
      - Note
      - Against
      - "On"
      - Offer
  /api/people/{id}/savenote:
    post:
      summary: Add a Note to a Person
      description: Add a note to a person.
      operationId: People_SaveNoteByidBynote
      x-api-path-slug: apipeopleidsavenote-post
      parameters:
      - in: path
        name: id
      - in: query
        name: note
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Person
  /api/progression/addprogressionnote:
    post:
      summary: Add a note to a purchasing role
      description: Add a note to a purchasing role.
      operationId: Progression_AddProgressionNoteByprogressionNoteCommandDataContract
      x-api-path-slug: apiprogressionaddprogressionnote-post
      parameters:
      - in: body
        name: progressionNoteCommandDataContract
        description: Details of the progression note
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Purchasing
      - Role
  /api/progression/milestone/addnote:
    post:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_AddMilestoneNoteBynoteDataContract
      x-api-path-slug: apiprogressionmilestoneaddnote-post
      parameters:
      - in: body
        name: noteDataContract
        description: Notes to be added
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/progression/milestones/reset:
    put:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_ResetRoleMilestonesBypurchasingRoleIdByroleId
      x-api-path-slug: apiprogressionmilestonesreset-put
      parameters:
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: roleId
        description: Sales role ID
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/todo/addtasknote:
    post:
      summary: Add note for a task
      description: Add note for a task.
      operationId: DefaultToDo_AddTaskNoteBynote
      x-api-path-slug: apitodoaddtasknote-post
      parameters:
      - in: body
        name: note
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Notea
      - Task
  /api/todo/addtodonote:
    post:
      summary: Add note for a ToDo
      description: Add note for a todo.
      operationId: DefaultToDo_AddToDoNoteBytoDoIdBynote
      x-api-path-slug: apitodoaddtodonote-post
      parameters:
      - in: body
        name: note
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: toDoId
      responses:
        200:
          description: OK
      tags:
      - Notea
      - ToDo
  /api/agency/updateportalcustomisation:
    put:
      summary: "THIS IS A TEMPORARY ENDPOINT TO Update a portal customisation against
        a brand within a branch.\r\nPLEASE NOTE: This will be replaced by a FE Tool
        in future. If not, Security must be improved."
      description: "This is a temporary endpoint to update a portal customisation
        against a brand within a branch.\r\nplease note: this will be replaced by
        a fe tool in future. if not, security must be improved.."
      operationId: Agency_UpdatePortalCustomisationByportalCustomisation
      x-api-path-slug: apiagencyupdateportalcustomisation-put
      parameters:
      - in: body
        name: portalCustomisation
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - THIS
      - IS
      - TEMPORARY
      - ENDPOINT
      - TO
      - ""
      - Portal
      - Customisation
      - Against
      - Brand
      - Within
      - Branch
      - PLEASE
      - 'NOTE:'
      - This
      - Will
      - Be
      - Replaced
      - By
      - FE
      - Tool
      - In
      - Future
      - ""
      - If
      - Not
      - ""
      - Security
      - Must
      - Be
      - Improved
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