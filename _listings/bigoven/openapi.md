swagger: "2.0"
x-collection-name: BigOven
x-complete: 1
info:
  title: Big Oven
  description: documentationthis-is-the-documentation-for-the-partner-endpoint-of-the-bigoven-recipe-and-grocery-list-api-the-update-brings-with-it-swaggerbased-documentation--swaggerhttpswagger-io-is-an-emerging-standard-for-describing-restbased-apis-and-with-this-swaggercompliant-endpoint-above-you-can-make-readytogo-interface-libraries-for-your-code-via-swaggercodegenhttpsgithub-comswaggerapiswaggercodegen--for-instance-its-easy-to-generate-libraries-for-node-js-java-ruby-asp-net-mvc-jquery-php-and-moreyou-can-also-try-out-the-endpoint-calls-with-your-own-api-key-right-here-on-this-page--be-sure-to-enter-your-api-key-above-to-use-the-try-it-out-buttons-on-this-page-start-heredevelopers-new-to-the-bigoven-api-should-start-with-this-version-not-with-the-legacy-api--well-be-making-improvements-to-this-api-over-time-and-doing-only-bug-fixes-on-the-v1-api-to-pretend-youre-a-bigoven-user-for-instance-to-get-your-recently-viewed-recipes-or-your-grocery-list-you-need-to-pass-in-basic-authentication-information-in-the-header-just-as-with-the-v1-api--we-do-now-require-that-you-make-all-calls-via-https--you-need-to-pass-your-api-key-in-with-every-call-though-this-can-now-be-done-on-the-header-send-a-request-header-xbigovenapikey-set-to-your-api-key-value-e-g--requestxbigovenapikeyyourkeyhere-migration-notesfor-existing-partners-we-encourage-you-to-migratehttpapi2-bigoven-com-and-while-at-this-writing-we-have-no-hardandfast-termination-date-for-the-v1-api-we-strongly-prefer-that-you-migrate-by-january-1-2017--while-the-changes-arent-overly-complex-there-are-several-breaking-changes-including-refactoring-of-recipe-search-and-results-and-removal-of-support-for-xml--this-is-not-a-simply-plugandplay-replacement-to-the-v1-api--with-respect-to-an-exclusive-focus-on-json-the-world-has-spoken-and-it-prefers-json-for-restbased-apis--weve-taken-numerous-steps-to-refactor-the-api-to-make-it-more-restcompliant--note-that-this-v2-api-will-be-the-preferred-api-from-this-point-onward-so-we-encourage-developers-to-migrate-to-this-new-format--we-have-put-together-some-migration-noteswebdocumentationmigrationtov2-that-we-encourage-you-to-read-carefully-photossee-our-photos-documentationhttpapi2-bigoven-comwebdocumentationrecipeimages--for-more-information-on-usage-of-this-api-including-features-pricing-rate-limits-terms-and-conditions-please-visit-the-bigoven-api-websitehttpapi2-bigoven-com-
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