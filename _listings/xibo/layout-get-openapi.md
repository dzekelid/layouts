---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Search Layouts
  description: Search for Layouts viewable by this user
  termsOfService: http://xibo.org.uk/legal
  version: 1.0.0
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /campaign/layout/assign/{campaignId}:
    post:
      summary: Assign Layouts
      description: Assign Layouts to a Campaign
      operationId: campaignAssignLayout
      x-api-path-slug: campaignlayoutassigncampaignid-post
      parameters:
      - in: path
        name: campaignId
        description: The Campaign ID
      - in: formData
        name: layoutId
        description: Array of Layout ID/Display Orders to Assign
      - in: formData
        name: unassignLayoutId
        description: Array of Layout ID/Display Orders to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Layouts
  /displaygroup/{displayGroupId}/layout/assign:
    post:
      summary: Assign one or more Layouts items to a Display Group
      description: Adds the provided Layouts to the Display Group
      operationId: displayGroupLayoutsAssign
      x-api-path-slug: displaygroupdisplaygroupidlayoutassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to assign to
      - in: formData
        name: layoutId
        description: The Layouts Ids to assign
      - in: formData
        name: unassignLayoutId
        description: Optional array of Layouts Id to unassign
      responses:
        200:
          description: OK
      tags:
      - Assign
      - More
      - Layouts
      - Items
      - To
      - Display
      - Group
  /layout:
    get:
      summary: Search Layouts
      description: Search for Layouts viewable by this user
      operationId: layoutSearch
      x-api-path-slug: layout-get
      parameters:
      - in: formData
        name: embed
        description: Embed related data such as regions, playlists, tags, etc
      - in: formData
        name: exactTags
        description: A flag indicating whether to treat the tags filter as an exact
          match
      - in: formData
        name: layout
        description: Filter by partial Layout name
      - in: formData
        name: layoutId
        description: Filter by Layout Id
      - in: formData
        name: ownerUserGroupId
        description: Filter by users in this UserGroupId
      - in: formData
        name: retired
        description: Filter by retired flag
      - in: formData
        name: tags
        description: Filter by Tags
      - in: formData
        name: userId
        description: Filter by user Id
      responses:
        200:
          description: OK
      tags:
      - Search
      - Layouts
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