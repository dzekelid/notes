---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Delete Projects Snippets Snippet Notes Note Award Emoji Award
  version: 1.0.0
  description: Delete projects snippets snippet notes note award emoji award.
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/issues/{issue_id}/notes/{note_id}/award_emoji:
    get:
      summary: Get Projects Issues Issue Notes Note Award Emoji
      description: Get projects issues issue notes note award emoji.
      operationId: getV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emoji-get
      parameters:
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
    post:
      summary: Post Projects Issues Issue Notes Note Award Emoji
      description: Post projects issues issue notes note award emoji.
      operationId: postV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emoji-post
      parameters:
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: formData
        name: name
        description: The name of a award_emoji (without colons)
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
  /v3/projects/{id}/issues/{issue_id}/notes/{note_id}/award_emoji/{award_id}:
    get:
      summary: Get Projects Issues Issue Notes Note Award Emoji Award
      description: Get projects issues issue notes note award emoji award.
      operationId: getV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emojiaward-id-get
      parameters:
      - in: path
        name: award_id
        description: The ID of the award
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
      - Award
    delete:
      summary: Delete Projects Issues Issue Notes Note Award Emoji Award
      description: Delete projects issues issue notes note award emoji award.
      operationId: deleteV3ProjectsIdIssuesIssueIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidissuesissue-idnotesnote-idaward-emojiaward-id-delete
      parameters:
      - in: path
        name: award_id
        description: The ID of an award emoji
      - in: path
        name: id
      - in: path
        name: issue_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Issue
      - Notes
      - Note
      - Award
      - Emoji
      - Award
  /v3/projects/{id}/merge_requests/{merge_request_id}/notes/{note_id}/award_emoji:
    get:
      summary: Get Projects Merge Requests Merge Request Notes Note Award Emoji
      description: Get projects merge requests merge request notes note award emoji.
      operationId: getV3ProjectsIdMergeRequestsMergeRequestIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidmerge-requestsmerge-request-idnotesnote-idaward-emoji-get
      parameters:
      - in: path
        name: id
      - in: path
        name: merge_request_id
      - in: path
        name: note_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Merge
      - Request
      - Notes
      - Note
      - Award
      - Emoji
    post:
      summary: Post Projects Merge Requests Merge Request Notes Note Award Emoji
      description: Post projects merge requests merge request notes note award emoji.
      operationId: postV3ProjectsIdMergeRequestsMergeRequestIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidmerge-requestsmerge-request-idnotesnote-idaward-emoji-post
      parameters:
      - in: path
        name: id
      - in: path
        name: merge_request_id
      - in: formData
        name: name
        description: The name of a award_emoji (without colons)
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Merge
      - Request
      - Notes
      - Note
      - Award
      - Emoji
  /v3/projects/{id}/merge_requests/{merge_request_id}/notes/{note_id}/award_emoji/{award_id}:
    get:
      summary: Get Projects Merge Requests Merge Request Notes Note Award Emoji Award
      description: Get projects merge requests merge request notes note award emoji
        award.
      operationId: getV3ProjectsIdMergeRequestsMergeRequestIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidmerge-requestsmerge-request-idnotesnote-idaward-emojiaward-id-get
      parameters:
      - in: path
        name: award_id
        description: The ID of the award
      - in: path
        name: id
      - in: path
        name: merge_request_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Merge
      - Request
      - Notes
      - Note
      - Award
      - Emoji
      - Award
    delete:
      summary: Delete Projects Merge Requests Merge Request Notes Note Award Emoji
        Award
      description: Delete projects merge requests merge request notes note award emoji
        award.
      operationId: deleteV3ProjectsIdMergeRequestsMergeRequestIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidmerge-requestsmerge-request-idnotesnote-idaward-emojiaward-id-delete
      parameters:
      - in: path
        name: award_id
        description: The ID of an award emoji
      - in: path
        name: id
      - in: path
        name: merge_request_id
      - in: path
        name: note_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Merge
      - Request
      - Notes
      - Note
      - Award
      - Emoji
      - Award
  /v3/projects/{id}/snippets/{snippet_id}/notes/{note_id}/award_emoji:
    get:
      summary: Get Projects Snippets Snippet Notes Note Award Emoji
      description: Get projects snippets snippet notes note award emoji.
      operationId: getV3ProjectsIdSnippetsSnippetIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidsnippetssnippet-idnotesnote-idaward-emoji-get
      parameters:
      - in: path
        name: id
      - in: path
        name: note_id
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: path
        name: snippet_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Snippet
      - Notes
      - Note
      - Award
      - Emoji
    post:
      summary: Post Projects Snippets Snippet Notes Note Award Emoji
      description: Post projects snippets snippet notes note award emoji.
      operationId: postV3ProjectsIdSnippetsSnippetIdNotesNoteIdAwardEmoji
      x-api-path-slug: v3projectsidsnippetssnippet-idnotesnote-idaward-emoji-post
      parameters:
      - in: path
        name: id
      - in: formData
        name: name
        description: The name of a award_emoji (without colons)
      - in: path
        name: note_id
      - in: path
        name: snippet_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Snippet
      - Notes
      - Note
      - Award
      - Emoji
  /v3/projects/{id}/snippets/{snippet_id}/notes/{note_id}/award_emoji/{award_id}:
    get:
      summary: Get Projects Snippets Snippet Notes Note Award Emoji Award
      description: Get projects snippets snippet notes note award emoji award.
      operationId: getV3ProjectsIdSnippetsSnippetIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidsnippetssnippet-idnotesnote-idaward-emojiaward-id-get
      parameters:
      - in: path
        name: award_id
        description: The ID of the award
      - in: path
        name: id
      - in: path
        name: note_id
      - in: path
        name: snippet_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Snippet
      - Notes
      - Note
      - Award
      - Emoji
      - Award
    delete:
      summary: Delete Projects Snippets Snippet Notes Note Award Emoji Award
      description: Delete projects snippets snippet notes note award emoji award.
      operationId: deleteV3ProjectsIdSnippetsSnippetIdNotesNoteIdAwardEmojiAwardId
      x-api-path-slug: v3projectsidsnippetssnippet-idnotesnote-idaward-emojiaward-id-delete
      parameters:
      - in: path
        name: award_id
        description: The ID of an award emoji
      - in: path
        name: id
      - in: path
        name: note_id
      - in: path
        name: snippet_id
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Snippet
      - Notes
      - Note
      - Award
      - Emoji
      - Award
  /v3/projects/{id}/issues/{noteable_id}/notes:
    get:
      summary: Get Projects Issues Noteable Notes
      description: Get a list of project +noteable+ notes
      operationId: getV3ProjectsIdIssuesNoteableIdNotes
      x-api-path-slug: v3projectsidissuesnoteable-idnotes-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
    post:
      summary: Post Projects Issues Noteable Notes
      description: Post projects issues noteable notes.
      operationId: postV3ProjectsIdIssuesNoteableIdNotes
      x-api-path-slug: v3projectsidissuesnoteable-idnotes-post
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: formData
        name: created_at
        description: The creation date of the note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
  /v3/projects/{id}/issues/{noteable_id}/notes/{note_id}:
    get:
      summary: Get Projects Issues Noteable Notes Note
      description: Get projects issues noteable notes note.
      operationId: getV3ProjectsIdIssuesNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidissuesnoteable-idnotesnote-id-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
      - Note
    put:
      summary: Put Projects Issues Noteable Notes Note
      description: Put projects issues noteable notes note.
      operationId: putV3ProjectsIdIssuesNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidissuesnoteable-idnotesnote-id-put
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
      - Note
    delete:
      summary: Delete Projects Issues Noteable Notes Note
      description: Delete projects issues noteable notes note.
      operationId: deleteV3ProjectsIdIssuesNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidissuesnoteable-idnotesnote-id-delete
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Issues
      - Noteable
      - Notes
      - Note
  /v3/projects/{id}/merge_requests/{noteable_id}/notes:
    get:
      summary: Get Projects Merge Requests Noteable Notes
      description: Get projects merge requests noteable notes.
      operationId: getV3ProjectsIdMergeRequestsNoteableIdNotes
      x-api-path-slug: v3projectsidmerge-requestsnoteable-idnotes-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Noteable
      - Notes
    post:
      summary: Post Projects Merge Requests Noteable Notes
      description: Post projects merge requests noteable notes.
      operationId: postV3ProjectsIdMergeRequestsNoteableIdNotes
      x-api-path-slug: v3projectsidmerge-requestsnoteable-idnotes-post
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: formData
        name: created_at
        description: The creation date of the note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Noteable
      - Notes
  /v3/projects/{id}/merge_requests/{noteable_id}/notes/{note_id}:
    get:
      summary: Get Projects Merge Requests Noteable Notes Note
      description: Get projects merge requests noteable notes note.
      operationId: getV3ProjectsIdMergeRequestsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidmerge-requestsnoteable-idnotesnote-id-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Noteable
      - Notes
      - Note
    put:
      summary: Put Projects Merge Requests Noteable Notes Note
      description: Put projects merge requests noteable notes note.
      operationId: putV3ProjectsIdMergeRequestsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidmerge-requestsnoteable-idnotesnote-id-put
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Noteable
      - Notes
      - Note
    delete:
      summary: Delete Projects Merge Requests Noteable Notes Note
      description: Delete projects merge requests noteable notes note.
      operationId: deleteV3ProjectsIdMergeRequestsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidmerge-requestsnoteable-idnotesnote-id-delete
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Merge
      - Requests
      - Noteable
      - Notes
      - Note
  /v3/projects/{id}/snippets/{noteable_id}/notes:
    get:
      summary: Get Projects Snippets Noteable Notes
      description: Get a list of project +noteable+ notes
      operationId: getV3ProjectsIdSnippetsNoteableIdNotes
      x-api-path-slug: v3projectsidsnippetsnoteable-idnotes-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Noteable
      - Notes
    post:
      summary: Post Projects Snippets Noteable Notes
      description: Post projects snippets noteable notes.
      operationId: postV3ProjectsIdSnippetsNoteableIdNotes
      x-api-path-slug: v3projectsidsnippetsnoteable-idnotes-post
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: formData
        name: created_at
        description: The creation date of the note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Noteable
      - Notes
  /v3/projects/{id}/snippets/{noteable_id}/notes/{note_id}:
    get:
      summary: Get Projects Snippets Noteable Notes Note
      description: Get projects snippets noteable notes note.
      operationId: getV3ProjectsIdSnippetsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidsnippetsnoteable-idnotesnote-id-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Noteable
      - Notes
      - Note
    put:
      summary: Put Projects Snippets Noteable Notes Note
      description: Put projects snippets noteable notes note.
      operationId: putV3ProjectsIdSnippetsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidsnippetsnoteable-idnotesnote-id-put
      parameters:
      - in: formData
        name: body
        description: The content of a note
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Noteable
      - Notes
      - Note
    delete:
      summary: Delete Projects Snippets Noteable Notes Note
      description: Delete projects snippets noteable notes note.
      operationId: deleteV3ProjectsIdSnippetsNoteableIdNotesNoteId
      x-api-path-slug: v3projectsidsnippetsnoteable-idnotesnote-id-delete
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: noteable_id
        description: The ID of the noteable
      - in: path
        name: note_id
        description: The ID of a note
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Snippets
      - Noteable
      - Notes
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