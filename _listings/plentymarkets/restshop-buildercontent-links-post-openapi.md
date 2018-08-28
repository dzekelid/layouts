---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Link a content to a a layout container of a frontend plugin.
  description: Link a content to a a layout container of a frontend plugin..
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/listings/layout_templates:
    post:
      summary: Create new layout template
      description: Creates a new layout template.
      operationId: postRestListingsLayoutTemplates
      x-api-path-slug: restlistingslayout-templates-post
      parameters:
      - in: body
        name: /rest/listings/layout_templates
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Layout
      - Template
  /rest/listings/layout_templates/{id}:
    delete:
      summary: Delete a layout template
      description: Deletes a layout template by ID.
      operationId: deleteRestListingsLayoutTemplates
      x-api-path-slug: restlistingslayout-templatesid-delete
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Layout
      - Template
    get:
      summary: Get a layout template
      description: Gets a layout template by providing its ID.
      operationId: getRestListingsLayoutTemplates
      x-api-path-slug: restlistingslayout-templatesid-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Layout
      - Template
  /rest/shop_builder/content_links:
    post:
      summary: Link a content to a a layout container of a frontend plugin.
      description: Link a content to a a layout container of a frontend plugin..
      operationId: postRestShopBuilderContentLinks
      x-api-path-slug: restshop-buildercontent-links-post
      parameters:
      - in: body
        name: /rest/shop_builder/content_links
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Link
      - Content
      - To
      - A
      - Layout
      - Container
      - Of
      - Frontend
      - Plugin
  /rest/storage/frontend/object-url:
    get:
      summary: Get the URL for a layout document
      description: Gets the URL of a layout document. The storage key must be specified.
        The returned URL expires after 10 minutes.
      operationId: getRestStorageFrontendObjectUrl
      x-api-path-slug: reststoragefrontendobjecturl-get
      parameters:
      - in: query
        name: key
        description: The storage key for the frontend document to retrieve the URL
          for
      responses:
        200:
          description: OK
      tags:
      - URLa
      - Layout
      - Document
  /rest/storage/layout:
    delete:
      summary: Delete layout documents
      description: Deletes a list of layout documents from storage. A list of storage
        keys must be specified.
      operationId: deleteRestStorageLayout
      x-api-path-slug: reststoragelayout-delete
      parameters:
      - in: query
        name: keyList
        description: List of storage keys for the files to be deleted
      responses:
        200:
          description: OK
      tags:
      - Layout
      - Documents
    post:
      summary: Upload a layout document
      description: Uploads a layout document to storage. The storage key (i.e. file
        path) must be specified.
      operationId: postRestStorageLayout
      x-api-path-slug: reststoragelayout-post
      parameters:
      - in: query
        name: key
        description: The storage key for the layout document to upload
      responses:
        200:
          description: OK
      tags:
      - Upload
      - Layout
      - Document
  /rest/storage/layout/list:
    get:
      summary: List layout documents
      description: |-
        Lists up to 1000 layout documents per request. If more than 1000 layout documents are available,
        a <code>nextContinuationToken</code> is returned. Use this token to get the next (up to) 1000 layout documents.
        Use the same request and include a field with the key <code>continuationToken</code> as well as the returned
        token from the previous call as the value.

        Check the <code>isTruncated</code> field in the response to see if more results are available. If <code>isTruncated</code> is true,
        repeat the request using the token from the <code>nextContinuationToken</code> field of the previous response to get all
        results.
      operationId: getRestStorageLayoutList
      x-api-path-slug: reststoragelayoutlist-get
      parameters:
      - in: query
        name: continuationToken
        description: Token for listing the next (up to) 1000 layout documents
      responses:
        200:
          description: OK
      tags:
      - List
      - Layout
      - Documents
  /rest/storage/layout/object-url:
    get:
      summary: Get the URL for a layout document
      description: Gets the URL of a layout document. The storage key must be specified.
        The returned URL expires after 10 minutes.
      operationId: getRestStorageLayoutObjectUrl
      x-api-path-slug: reststoragelayoutobjecturl-get
      parameters:
      - in: query
        name: key
        description: The storage key for the layout document to retrieve the URL for
      responses:
        200:
          description: OK
      tags:
      - URLa
      - Layout
      - Document
  /rest/warehouses/layouts:
    post:
      summary: Create a warehouse location layout
      description: Creates a warehouse location layout
      operationId: postRestWarehousesLayouts
      x-api-path-slug: restwarehouseslayouts-post
      parameters:
      - in: query
        name: dimensionId
        description: The warehouse location dimension ID of the warehouse location
          level
      - in: query
        name: isActiveForPickupPath
        description: Active flag for pickup path of the warehouse location dimension
      - in: query
        name: label
        description: The label of the warehouse location
      - in: query
        name: level
        description: The level of the warehouse location dimension
      - in: query
        name: levelId
        description: The warehouse location level ID of the warehouse location
      - in: query
        name: name
        description: The name of the warehouse location dimension
      - in: query
        name: parentId
        description: The parent ID of the warehouse location dimension
      - in: query
        name: position
        description: The position of the warehouse location level
      - in: query
        name: purposeKey
        description: The location type key of the warehouse location
      - in: query
        name: separator
        description: The separator of the warehouse location dimension
      - in: query
        name: shortcut
        description: The shortcut of the warehouse location dimension
      - in: query
        name: statusKey
        description: The location status key of the warehouse location
      - in: query
        name: warehouseId
        description: The warehouse ID of the warehouse location dimension
      responses:
        200:
          description: OK
      tags:
      - Warehouse
      - Location
      - Layout
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