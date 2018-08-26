---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/dashboard/{id}/setlayout:
    put:
      summary: Set widget layout on dashboards
      description: Set widget layout on dashboards.
      operationId: Dashboard_SetWidgetLayoutByidBylayouts
      x-api-path-slug: apidashboardidsetlayout-put
      parameters:
      - in: path
        name: id
        description: Dashboard Id
      - in: body
        name: layouts
        description: Array of layout objects
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Widget
      - Layout
      - "On"
      - Dashboards
---