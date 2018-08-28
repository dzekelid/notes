swagger: "2.0"
x-collection-name: HERE
x-complete: 1
info:
  title: Weather API
  description: the-here-weather-api-provides-weather-forecasts-and-reports-on-current-weather-conditions-provides-information-on-severe-weather-alerts-provides-information-about-when-the-sun-and-moon-rise-and-set-and-the-phase-of-the-moonthis-example-set-works-with-version-1-2-4-or-higheradditional-information-can-be-found-on-developer-here-comhttpsdeveloper-here-comrestapisdocumentationweather
  version: 1.0.0
host: weather.cit.api.here.com
basePath: /weather/1.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /1/models-full/DM_12321.js:
    get:
      summary: Full Venue Model
      description: "*Request extended details of places found within a venue*\n\nA
        full model of a venue can be obtained by passing `models-full` in the path
        of the request URL and appending the `id` of the venue in question along with
        associated authentication credentials. \n  \n  Note that the client-side process
        formatting the JSON response may take some time in older browsers.\n\n\n\n*
        **app_id**  `text`\n \\- A 20 byte Base64 URL-safe encoded string used for
        the authentication of the client application.    You must include an `app_id`
        with every request.\n\n* **app_code**  `text`\n \\- A 20 byte Base64 URL-safe
        encoded string used for the authentication of the client application.    You
        must include an `app_code` with every request.\n\n* **Signature**  `text`\n
        \\- Signature\n\n* **Policy**  `text`\n \\- Policy\n\n* **Key-Pair-Id**  `text`\n
        \\- Key-Pair-Id"
      operationId: 1ModelsFullDM12321JsGet
      x-api-path-slug: 1modelsfulldm-12321-js-get
      parameters:
      - in: query
        name: app_code
      - in: query
        name: app_id
      - in: query
        name: Key-Pair-Id
      - in: query
        name: Policy
      - in: query
        name: Signature
      responses:
        200:
          description: OK
      tags:
      - Full
      - Venue
      - Model