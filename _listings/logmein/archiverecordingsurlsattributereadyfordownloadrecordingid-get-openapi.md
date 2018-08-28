---
swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 0
info:
  title: GoToAssist Remote Support Download Recordings
  description: "This method retrieves download links for a list of recordings. Each
    recording returns a link to the MP4 file, the .events file and the thumbnail.
    If a recording is not available for download then it will be omitted from the
    returned list. The archiving script may use the returned URLs to download each
    resource for the recording. The URLs will be valid for at least 48 hours. The
    URL contains a large random number so that the URL for recordings cannot be guessed.
    The response includes the recording start time to make it easier for the archiving
    script to place recordings in directories based on date. No more than 500 recordings
    can be requested at once.\n\nNote: Session recording must be enabled on the account
    in order to use this API method. To enable session recording, log in at https://app.gotoassist.com
    (link is external) and go to Configure > GoToAssist Settings > Enable Session
    Recording check box.\n\n  Response Parameters                  \n                    \n
    \   field      data type      description    \n    recordingId      number      The
    recordingId of the session recording to be downloaded    \n    recordingUrl      string
    \     The URL of MP4 recording file    \n    recordingStartTime      ISO 8601
    format*      The start time of recording    \n    eventsUrl      string      The
    URL of the events recording file    \n    thumbnailUrl      string      The URL
    of the thumbnail of recording file    \n    recordingSize      string      The
    size of the .mp4 file in bytes    \n\n* ISO 8601 format reference\n                    \nStatus
    Codes                    \n                    \n    Staus Code      description
    \         \n    200 OK      A list of URLs has been returned          \n    400
    Bad Request      Request may be malformed or property may be missing or invalid
    \         \n    403 Forbidden      Invalid authorization header or invalid recording
    Ids          \n    500 Internal Server Error      Unexpected server error"
  version: 1.0.0
host: api.getgo.com
basePath: /G2A/rest/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /archive/recordings:
    get:
      summary: Available Recordings
      description: "This method retrieves a list of all available recordings on the
        account. Only recordings which are available for transcoding or downloading
        will be returned. The recording IDs are always returned in the order in which
        the recordings were started (i.e., startTime order). The request must contain
        one or more of the following: accountKey, userKey or companyId. The list of
        recordings can be filtered by the request parameters listed below.\n\nNote:
        Session recording must be enabled on the account in order to use this API
        method. To enable session recording, log in at https://app.gotoassist.com
        (link is external) and go to Configure > GoToAssist Settings > Enable Session
        Recording check box.\n\n  Request Parameters                  \n  Each request
        must contain one or more of the following: accountKey, userKey or companyId.
        \                 \n                    \n    field      data type      description
        \   \n    accountKey      number      The account key associated with the
        recording ( available in the Get Screen Sharing Session Info (link is external)
        method response )    \n    userKey      number      The user key of the technician
        who started the recorded session (available in the Authentication (link is
        external) API method response)    \n    companyId      number      The companyId
        associated with the recording for unattended support sessions only ( available
        in the Get Companies (link is external) API method response )    \n    sessionType
        *      number      The type of session: attended (0) or unattended (1)    \n
        \   fromTime *      ISO 8601 format **      The oldest sessions that should
        be retrieved (startTime must be greater than or equal to fromTime)    \n    toTime
        *      ISO 8601 format **      The most recent sessions that should be retrieved
        (startTime must be greater than or equal to fromTime)    \n    timePeriod
        *      number      The recordings within a Time Period, starting from currentDate
        (ex: \u201DtimePeriod=30\u201D would retrieve the last 30 days\u2019 recordings)
        \   \n    archived *      number      The option to include only archived
        recordings, as follows: include only archived recordings (1) or include only
        non-archived recordings (0 or omit)    \n                    \n* Optional
        \                   \n** ISO 8601 format reference                    \n                    \n
        \ Response Parameters                  \n  No more than 500 recordings at
        a time will be returned for readyForTranscode or readyForDownload.                  \n
        \                   \n    field      data type      description    \n    readyForTranscode
        \     array      A list of recordingIds for recordings that are ready to be
        transcoded    \n    readyForDownload      array      A list of recordingIds
        for recordings that are ready to be downloaded    \n                    \n
        \                   \nStatus Codes                    \n                    \n
        \   Staus Code      description          \n    200 OK      Recordings retrieved
        successfully          \n    400 Bad Request      Request may be malformed
        or property may be missing or invalid          \n    403 Forbidden      Invalid
        authorization header or invalid userKey, accountKey or companyId          \n
        \   500 Internal Server Error      Unexpected server error"
      operationId: ArchiveRecordingsGet
      x-api-path-slug: archiverecordings-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: userKey
      responses:
        200:
          description: OK
      tags:
      - Available
      - Recordings
  /archive/recordings/archived/{recordingIDs}:
    put:
      summary: Mark Recordings as Archived
      description: "This method marks a list of recordings as archived by setting
        their archived flag to \u201Ctrue.\u201D No more than 500 recordings can be
        marked as archived once.\n\nNote: Session recording must be enabled on the
        account in order to use this API method. To enable session recording, log
        in at https://app.gotoassist.com (link is external) and go to Configure >
        GoToAssist Settings > Enable Session Recording check box.\n\n  Request Parameters
        \                   \n                      \n    field        data type      description
        \   \n    recordingIds        array      A list of recordingIDs for the recordings
        to be archived    \n\n\nStatus Codes                \n                \n    Staus
        Code        description    \n    204 No Content        Recordings have been
        archived    \n    400 Bad Request        Request may be malformed or property
        may be missing or invalid    \n    403 Forbidden        Invalid authorization
        header or invalid recordingIDs    \n    500 Internal Server Error        Unexpected
        server error"
      operationId: ArchiveRecordingsArchivedByRecordingIDsPut
      x-api-path-slug: archiverecordingsarchivedrecordingids-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: recordingIDs
      responses:
        200:
          description: OK
      tags:
      - Mark
      - Recordings
      - As
      - Archived
  /archive/recordings/transcode/{readyForTranscodeRecordingIds}:
    post:
      summary: Transcode Recordings
      description: "This method requests that a list of recordings be transcoded;
        once the API passes successfully, transcoding will be initiated for each of
        the recordings in the list. A result of \u201C204\u201D will be returned,
        regardless of the current state of the recordings (i.e., even if they are
        already transcoded). No more than 500 recordings can be transcoded at once.\n\nNote:
        Session recording must be enabled on the account in order to use this API
        method. To enable session recording, log in at https://app.gotoassist.com
        (link is external) and go to Configure > GoToAssist Settings > Enable Session
        Recording check box.\n\n  Request Parameters                    \n                      \n
        \   field        data type      description    \n    recordingIds        array
        \     A list of RecordingIds for the recordings to be transcoded    \n                      \n\nStatus
        Codes                \n                \n    Staus Code        description
        \   \n    204 No Content        Transcoding initiated    \n    400 Bad Request
        \       Request may be malformed or property may be missing or invalid    \n
        \   403 Forbidden        Invalid authorization header or invalid recordingIDs
        \   \n    500 Internal Server Error        Unexpected server error"
      operationId: ArchiveRecordingsTranscodeByReadyForTranscodeRecordingIdsPost
      x-api-path-slug: archiverecordingstranscodereadyfortranscoderecordingids-post
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: readyForTranscodeRecordingIds
      responses:
        200:
          description: OK
      tags:
      - Transcode
      - Recordings
  /archive/recordings/urls[&{attribute}={readyForDownloadRecordingId}]:
    get:
      summary: Download Recordings
      description: "This method retrieves download links for a list of recordings.
        Each recording returns a link to the MP4 file, the .events file and the thumbnail.
        If a recording is not available for download then it will be omitted from
        the returned list. The archiving script may use the returned URLs to download
        each resource for the recording. The URLs will be valid for at least 48 hours.
        The URL contains a large random number so that the URL for recordings cannot
        be guessed. The response includes the recording start time to make it easier
        for the archiving script to place recordings in directories based on date.
        No more than 500 recordings can be requested at once.\n\nNote: Session recording
        must be enabled on the account in order to use this API method. To enable
        session recording, log in at https://app.gotoassist.com (link is external)
        and go to Configure > GoToAssist Settings > Enable Session Recording check
        box.\n\n  Response Parameters                  \n                    \n    field
        \     data type      description    \n    recordingId      number      The
        recordingId of the session recording to be downloaded    \n    recordingUrl
        \     string      The URL of MP4 recording file    \n    recordingStartTime
        \     ISO 8601 format*      The start time of recording    \n    eventsUrl
        \     string      The URL of the events recording file    \n    thumbnailUrl
        \     string      The URL of the thumbnail of recording file    \n    recordingSize
        \     string      The size of the .mp4 file in bytes    \n\n* ISO 8601 format
        reference\n                    \nStatus Codes                    \n                    \n
        \   Staus Code      description          \n    200 OK      A list of URLs
        has been returned          \n    400 Bad Request      Request may be malformed
        or property may be missing or invalid          \n    403 Forbidden      Invalid
        authorization header or invalid recording Ids          \n    500 Internal
        Server Error      Unexpected server error"
      operationId: ArchiveRecordingsUrlsAPIGet
      x-api-path-slug: archiverecordingsurlsattributereadyfordownloadrecordingid-get
      parameters:
      - in: header
        name: Accept
      - in: path
        name: attribute
      - in: header
        name: Content-Type
      - in: path
        name: readyForDownloadRecordingId
      responses:
        200:
          description: OK
      tags:
      - Download
      - Recordings
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