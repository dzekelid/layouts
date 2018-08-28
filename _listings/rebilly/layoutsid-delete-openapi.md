---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 0
info:
  title: Rebilly Delete a layout
  description: Delete a layout with predefined identifier string
  termsOfService: https://www.rebilly.com/terms/
  contact:
    name: Rebilly API Support
    url: https://www.rebilly.com/contact/
    email: integrations@rebilly.com
  version: "2.1"
host: api.rebilly.com
basePath: /v2.1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /layouts:
    get:
      summary: Retrieve a layout list
      description: Retrieve a layout list
      operationId: retrieve-a-layout-list
      x-api-path-slug: layouts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Layout
      - List
    post:
      summary: Create a layout
      description: Create a layout
      operationId: create-a-layout
      x-api-path-slug: layouts-post
      parameters:
      - in: body
        name: body
        description: Layout resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Layout
  /layouts/{id}:
    delete:
      summary: Delete a layout
      description: Delete a layout with predefined identifier string
      operationId: delete-a-layout-with-predefined-identifier-string
      x-api-path-slug: layoutsid-delete
      responses:
        200:
          description: OK
      tags:
      - Layout
    get:
      summary: Retrieve a layout
      description: Retrieve a layout with specified identifier string
      operationId: retrieve-a-layout-with-specified-identifier-string
      x-api-path-slug: layoutsid-get
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Layout
    put:
      summary: Create or update a layout with predefined ID
      description: Create or update a layout with predefined identifier string
      operationId: create-or-update-a-layout-with-predefined-identifier-string
      x-api-path-slug: layoutsid-put
      parameters:
      - in: body
        name: body
        description: Layout resource
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Update
      - Layout
      - Predefined
      - ID
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