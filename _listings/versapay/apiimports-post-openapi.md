---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay Import a CSV File
  description: |-
    When uploading a CSV-formatted file it???s helpful to use your language/framework tooling to simplify the [multipart/form-data](https://www.ietf.org/rfc/rfc2388.txt) file upload.
    ### Size Limit
    The file cannot exceed 25MB.
    ### Layouts
    Please contact support@versapay.com or reach out to your implementation specialist for standard inbound CSV file layouts.
  contact:
    name: VersaPay Support
    url: https://www.versapay.com/support
    email: support@versapay.com
  version: 1.0.0
host: secure.versapay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/imports:
    post:
      summary: Import a CSV File
      description: |-
        When uploading a CSV-formatted file it???s helpful to use your language/framework tooling to simplify the [multipart/form-data](https://www.ietf.org/rfc/rfc2388.txt) file upload.
        ### Size Limit
        The file cannot exceed 25MB.
        ### Layouts
        Please contact support@versapay.com or reach out to your implementation specialist for standard inbound CSV file layouts.
      operationId: importBatchFile
      x-api-path-slug: apiimports-post
      parameters:
      - in: formData
        name: file
        description: The file to upload
      - in: formData
        name: filename
        description: Name of original file
      responses:
        200:
          description: OK
      tags:
      - ImportCSV
      - File
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