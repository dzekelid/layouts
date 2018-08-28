---
swagger: "2.0"
x-collection-name: Xibo
x-complete: 0
info:
  title: Xibo API Layout Status
  description: Calculate the Layout status and return a Layout
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
    post:
      summary: Add a Layout
      description: Add a new Layout to the CMS
      operationId: layoutAdd
      x-api-path-slug: layout-post
      parameters:
      - in: formData
        name: description
        description: The layout description
      - in: formData
        name: layoutId
        description: If the Layout should be created with a Template, provide the
          ID, otherwise dont provide
      - in: formData
        name: name
        description: The layout name
      - in: formData
        name: resolutionId
        description: If a Template is not provided, provide the resolutionId for this
          Layout
      responses:
        200:
          description: OK
      tags:
      - Layout
  /display/defaultlayout/{displayId}:
    post:
      summary: Set Default Layout
      description: Sent the default Layout on this Display
      operationId: displayDefaultLayout
      x-api-path-slug: displaydefaultlayoutdisplayid-post
      parameters:
      - in: path
        name: displayId
        description: The Display ID
      - in: formData
        name: layoutId
        description: The Layout ID
      responses:
        200:
          description: OK
      tags:
      - Set
      - Default
      - Layout
  /displaygroup/{displayGroupId}/layout/unassign:
    post:
      summary: Unassign one or more Layout items from a Display Group
      description: Removes the provided from the Display Group
      operationId: displayGroupLayoutUnassign
      x-api-path-slug: displaygroupdisplaygroupidlayoutunassign-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group to unassign from
      - in: formData
        name: layoutId
        description: The Layout Ids to unassign
      responses:
        200:
          description: OK
      tags:
      - Unassign
      - More
      - Layout
      - Items
      - From
      - Display
      - Group
  /displaygroup/{displayGroupId}/action/changeLayout:
    post:
      summary: 'Action: Change Layout'
      description: Send the change layout action to this DisplayGroup
      operationId: displayGroupActionChangeLayout
      x-api-path-slug: displaygroupdisplaygroupidactionchangelayout-post
      parameters:
      - in: formData
        name: changeMode
        description: Whether to queue or replace with this action
      - in: path
        name: displayGroupId
        description: The Display Group Id
      - in: formData
        name: downloadRequired
        description: Flag indicating whether the player should perform a collect before
          playing the Layout
      - in: formData
        name: duration
        description: The duration in seconds for this Layout change to remain in effect
      - in: formData
        name: layoutId
        description: The Layout Id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Change
      - Layout
  /displaygroup/{displayGroupId}/action/overlayLayout:
    post:
      summary: 'Action: Overlay Layout'
      description: Send the overlay layout action to this DisplayGroup
      operationId: displayGroupActionOverlayLayout
      x-api-path-slug: displaygroupdisplaygroupidactionoverlaylayout-post
      parameters:
      - in: path
        name: displayGroupId
        description: The Display Group Id
      - in: formData
        name: downloadRequired
        description: Flag indicating whether the player should perform a collect before
          adding the Overlay
      - in: formData
        name: duration
        description: The duration in seconds for this Overlay to remain in effect
      - in: formData
        name: layoutId
        description: The Layout Id
      responses:
        200:
          description: OK
      tags:
      - 'Action:'
      - Overlay
      - Layout
  /layout/{layoutId}:
    put:
      summary: Edit Layout
      description: Edit a Layout
      operationId: layoutEdit
      x-api-path-slug: layoutlayoutid-put
      parameters:
      - in: formData
        name: backgroundColor
        description: A HEX color to use as the background color of this Layout
      - in: formData
        name: backgroundImageId
        description: A media ID to use as the background image for this Layout
      - in: formData
        name: backgroundzIndex
        description: The Layer Number to use for the background
      - in: formData
        name: description
        description: The Layout Description
      - in: path
        name: layoutId
      - in: formData
        name: name
        description: The Layout Name
      - in: formData
        name: resolutionId
        description: The Resolution ID to use on this Layout
      - in: formData
        name: retired
        description: A flag indicating whether this Layout is retired
      - in: formData
        name: tags
        description: A comma separated list of Tags
      responses:
        200:
          description: OK
      tags:
      - Edit
      - Layout
    delete:
      summary: Delete Layout
      description: Delete a Layout
      operationId: layoutDelete
      x-api-path-slug: layoutlayoutid-delete
      parameters:
      - in: path
        name: layoutId
        description: The Layout ID to Delete
      responses:
        200:
          description: OK
      tags:
      - Layout
  /layout/retire/{layoutId}:
    put:
      summary: Retire Layout
      description: Retire a Layout so that it isn't available to Schedule. Existing
        Layouts will still be played
      operationId: layoutRetire
      x-api-path-slug: layoutretirelayoutid-put
      parameters:
      - in: path
        name: layoutId
        description: The Layout ID
      responses:
        200:
          description: OK
      tags:
      - Retire
      - Layout
  /layout/copy/{layoutId}:
    post:
      summary: Copy Layout
      description: Copy a Layout, providing a new name if applicable
      operationId: layoutCopy
      x-api-path-slug: layoutcopylayoutid-post
      parameters:
      - in: formData
        name: copyMediaFiles
        description: Flag indicating whether to make new Copies of all Media Files
          assigned to the Layout being Copied
      - in: formData
        name: description
        description: The Description for the new Layout
      - in: path
        name: layoutId
        description: The Layout ID to Copy
      - in: formData
        name: name
        description: The name for the new Layout
      responses:
        200:
          description: OK
      tags:
      - Copy
      - Layout
  /layout/{layoutId}/tag:
    post:
      summary: Tag Layout
      description: Tag a Layout with one or more tags
      operationId: layoutTag
      x-api-path-slug: layoutlayoutidtag-post
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to Tag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Tag
      - Layout
  /layout/{layoutId}/untag:
    post:
      summary: Untag Layout
      description: Untag a Layout with one or more tags
      operationId: layoutUntag
      x-api-path-slug: layoutlayoutiduntag-post
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to Untag
      - in: formData
        name: tag
        description: An array of tags
      responses:
        200:
          description: OK
      tags:
      - Untag
      - Layout
  /layout/status/{layoutId}:
    get:
      summary: Layout Status
      description: Calculate the Layout status and return a Layout
      operationId: layoutStatus
      x-api-path-slug: layoutstatuslayoutid-get
      parameters:
      - in: path
        name: layoutId
        description: The Layout Id to get the status
      responses:
        200:
          description: OK
      tags:
      - Layout
      - Status
  /template/{layoutId}:
    post:
      summary: Add a template from a Layout
      description: Use the provided layout as a base for a new template
      operationId: template.add.from.layout
      x-api-path-slug: templatelayoutid-post
      parameters:
      - in: formData
        name: description
        description: A description of the Template
      - in: formData
        name: includeWidgets
        description: Flag indicating whether to include the widgets in the Template
      - in: path
        name: layoutId
        description: The Layout ID
      - in: formData
        name: name
        description: The Template Name
      - in: formData
        name: tags
        description: Comma separated list of Tags for the template
      responses:
        200:
          description: OK
      tags:
      - Template
      - From
      - Layout
  /playlist/widget/audio/{playlistId}:
    post:
      summary: Parameters for editing existing audio widget on a layout
      description: Parameters for editing existing audio widget on a layout, for adding
        new audio, please refer to POST /library documentation
      operationId: WidgetAudioEdit
      x-api-path-slug: playlistwidgetaudioplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the audio loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the audio be muted?
      - in: formData
        name: name
        description: Edit Only - The Widget name
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Audio
      - Widget
      - "On"
      - Layout
  /playlist/widget/image/{playlistId}:
    post:
      summary: Parameters for editing existing image on a layout
      description: Parameters for editing existing image on a layout, for adding new
        images, please refer to POST /library documentation
      operationId: WidgetImageEdit
      x-api-path-slug: playlistwidgetimageplaylistid-post
      parameters:
      - in: formData
        name: alignId
        description: Edit only - Horizontal alignment - left, center, bottom
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: scaleTypeId
        description: 'Edit only - Select scale type available options: center, stretch'
      - in: formData
        name: useDuration
        description: Edit only (0, 1) Select 1 only if you will provide duration parameter
          as well
      - in: formData
        name: valignId
        description: Edit only - Vertical alignment - top, middle, bottom
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Image
      - "On"
      - Layout
  /playlist/widget/pdf/{playlistId}:
    post:
      summary: Parameters for editing existing pdf on a layout
      description: Parameters for editing existing pdf on a layout, for adding new
        files, please refer to POST /library documentation
      operationId: WidgetPdfEdit
      x-api-path-slug: playlistwidgetpdfplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: useDuration
        description: (0, 1) Select 1 only if you will provide duration parameter as
          well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Pdf
      - "On"
      - Layout
  /playlist/widget/video/{playlistId}:
    post:
      summary: Parameters for editing existing video on a layout
      description: Parameters for editing existing video on a layout, for adding new
        videos, please refer to POST /library documentation
      operationId: WidgetVideoEdit
      x-api-path-slug: playlistwidgetvideoplaylistid-post
      parameters:
      - in: formData
        name: duration
        description: Edit Only - The Widget Duration
      - in: formData
        name: loop
        description: Edit only - Flag (0, 1) Should the video loop (only for duration
          > 0 )?
      - in: formData
        name: mute
        description: Edit only - Flag (0, 1) Should the video be muted?
      - in: formData
        name: name
        description: Edit only - Optional Widget Name
      - in: formData
        name: scaleTypeId
        description: 'How should the video be scaled, available options: aspect, stretch'
      - in: formData
        name: useDuration
        description: Edit Only - (0, 1) Select 1 only if you will provide duration
          parameter as well
      responses:
        200:
          description: OK
      tags:
      - Parametersediting
      - Existing
      - Video
      - "On"
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