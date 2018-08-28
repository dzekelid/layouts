---
name: Plentymarkets
x-slug: plentymarkets
description: plentymarkets is an all-in-one e-commerce ERP solution, which combines
  a comprehensive stock management system with a versatile shop system and effortless
  multichannel sales. Thanks to comprehensive functions and interfaces that include
  all steps of the e-commerce value chain, you can use the cloud based software to
  completely automate all of your e-business processes as well as your companys own
  individual processes.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
x-kinRank: "7"
x-alexaRank: ""
tags: Layouts
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/apis.md
specificationVersion: "0.14"
apis:
- name: plentymarkets REST-API - Create new layout template
  x-api-slug: restlistingslayout-templates-post
  description: Creates a new layout template.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templates-post-openapi.md
- name: plentymarkets REST-API - Delete a layout template
  x-api-slug: restlistingslayout-templatesid-delete
  description: Deletes a layout template by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-delete-openapi.md
- name: plentymarkets REST-API - Get a layout template
  x-api-slug: restlistingslayout-templatesid-get
  description: Gets a layout template by providing its ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-get-openapi.md
- name: plentymarkets REST-API - Link a content to a a layout container of a frontend
    plugin.
  x-api-slug: restshop-buildercontent-links-post
  description: Link a content to a a layout container of a frontend plugin..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restshop-buildercontent-links-post-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragefrontendobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragefrontendobjecturl-get-openapi.md
- name: plentymarkets REST-API - Delete layout documents
  x-api-slug: reststoragelayout-delete
  description: Deletes a list of layout documents from storage. A list of storage
    keys must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-delete-openapi.md
- name: plentymarkets REST-API - Upload a layout document
  x-api-slug: reststoragelayout-post
  description: Uploads a layout document to storage. The storage key (i.e. file path)
    must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-post-openapi.md
- name: plentymarkets REST-API - List layout documents
  x-api-slug: reststoragelayoutlist-get
  description: |-
    Lists up to 1000 layout documents per request. If more than 1000 layout documents are available,
    a <code>nextContinuationToken</code> is returned. Use this token to get the next (up to) 1000 layout documents.
    Use the same request and include a field with the key <code>continuationToken</code> as well as the returned
    token from the previous call as the value.

    Check the <code>isTruncated</code> field in the response to see if more results are available. If <code>isTruncated</code> is true,
    repeat the request using the token from the <code>nextContinuationToken</code> field of the previous response to get all
    results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutlist-get-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragelayoutobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutobjecturl-get-openapi.md
- name: plentymarkets REST-API - Create a warehouse location layout
  x-api-slug: restwarehouseslayouts-post
  description: Creates a warehouse location layout
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restwarehouseslayouts-post-openapi.md
- name: plentymarkets REST-API - Create new layout template
  x-api-slug: restlistingslayout-templates-post
  description: Creates a new layout template.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templates-post-openapi.md
- name: plentymarkets REST-API - Delete a layout template
  x-api-slug: restlistingslayout-templatesid-delete
  description: Deletes a layout template by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-delete-openapi.md
- name: plentymarkets REST-API - Get a layout template
  x-api-slug: restlistingslayout-templatesid-get
  description: Gets a layout template by providing its ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-get-openapi.md
- name: plentymarkets REST-API - Link a content to a a layout container of a frontend
    plugin.
  x-api-slug: restshop-buildercontent-links-post
  description: Link a content to a a layout container of a frontend plugin..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restshop-buildercontent-links-post-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragefrontendobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragefrontendobjecturl-get-openapi.md
- name: plentymarkets REST-API - Delete layout documents
  x-api-slug: reststoragelayout-delete
  description: Deletes a list of layout documents from storage. A list of storage
    keys must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-delete-openapi.md
- name: plentymarkets REST-API - Upload a layout document
  x-api-slug: reststoragelayout-post
  description: Uploads a layout document to storage. The storage key (i.e. file path)
    must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-post-openapi.md
- name: plentymarkets REST-API - List layout documents
  x-api-slug: reststoragelayoutlist-get
  description: |-
    Lists up to 1000 layout documents per request. If more than 1000 layout documents are available,
    a <code>nextContinuationToken</code> is returned. Use this token to get the next (up to) 1000 layout documents.
    Use the same request and include a field with the key <code>continuationToken</code> as well as the returned
    token from the previous call as the value.

    Check the <code>isTruncated</code> field in the response to see if more results are available. If <code>isTruncated</code> is true,
    repeat the request using the token from the <code>nextContinuationToken</code> field of the previous response to get all
    results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutlist-get-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragelayoutobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutobjecturl-get-openapi.md
- name: plentymarkets REST-API - Create a warehouse location layout
  x-api-slug: restwarehouseslayouts-post
  description: Creates a warehouse location layout
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restwarehouseslayouts-post-openapi.md
- name: plentymarkets REST-API - Create a warehouse location layout
  x-api-slug: restwarehouseslayouts-post
  description: Creates a warehouse location layout
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restwarehouseslayouts-post-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragelayoutobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutobjecturl-get-openapi.md
- name: plentymarkets REST-API - List layout documents
  x-api-slug: reststoragelayoutlist-get
  description: |-
    Lists up to 1000 layout documents per request. If more than 1000 layout documents are available,
    a <code>nextContinuationToken</code> is returned. Use this token to get the next (up to) 1000 layout documents.
    Use the same request and include a field with the key <code>continuationToken</code> as well as the returned
    token from the previous call as the value.

    Check the <code>isTruncated</code> field in the response to see if more results are available. If <code>isTruncated</code> is true,
    repeat the request using the token from the <code>nextContinuationToken</code> field of the previous response to get all
    results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayoutlist-get-openapi.md
- name: plentymarkets REST-API - Upload a layout document
  x-api-slug: reststoragelayout-post
  description: Uploads a layout document to storage. The storage key (i.e. file path)
    must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-post-openapi.md
- name: plentymarkets REST-API - Delete layout documents
  x-api-slug: reststoragelayout-delete
  description: Deletes a list of layout documents from storage. A list of storage
    keys must be specified.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragelayout-delete-openapi.md
- name: plentymarkets REST-API - Get the URL for a layout document
  x-api-slug: reststoragefrontendobjecturl-get
  description: Gets the URL of a layout document. The storage key must be specified.
    The returned URL expires after 10 minutes.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/reststoragefrontendobjecturl-get-openapi.md
- name: plentymarkets REST-API - Link a content to a a layout container of a frontend
    plugin.
  x-api-slug: restshop-buildercontent-links-post
  description: Link a content to a a layout container of a frontend plugin..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restshop-buildercontent-links-post-openapi.md
- name: plentymarkets REST-API - Get a layout template
  x-api-slug: restlistingslayout-templatesid-get
  description: Gets a layout template by providing its ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-get-openapi.md
- name: plentymarkets REST-API - Delete a layout template
  x-api-slug: restlistingslayout-templatesid-delete
  description: Deletes a layout template by ID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templatesid-delete-openapi.md
- name: plentymarkets REST-API - Create new layout template
  x-api-slug: restlistingslayout-templates-post
  description: Creates a new layout template.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/plentymarkets.png
  humanURL: http://www.plentymarkets.co.uk
  baseURL: https://example.com//
  tags: ERP, Service API, Relative Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/layouts/master/_listings/plentymarkets/restlistingslayout-templates-post-openapi.md
x-common:
- type: x-blog-rss
  url: https://www.plentymarkets.co.uk/?ActionCall=WebActionRSS&rrss_id=1
- type: x-github
  url: https://github.com/plentymarkets
- type: x-twitter
  url: https://twitter.com/plentymarketsuk
- type: x-website
  url: http://www.plentymarkets.co.uk
- type: x-api-gallery
  url: http://pivotal.tracker.api.gallery.streamdata.io
- type: x-api-stack
  url: http://plentymarkets.stack.network
- type: x-blog
  url: https://www.plentymarkets.co.uk/blog/
- type: x-pricing
  url: https://www.plentymarkets.co.uk/prices/
- type: x-website
  url: https://www.plentymarkets.co.uk
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---