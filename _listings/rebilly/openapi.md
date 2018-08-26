---
swagger: "2.0"
x-collection-name: Rebilly
x-complete: 1
info:
  title: Rebilly
  description: -introductionthe-rebilly-api-is-built-on-http---our-api-is-restful---it-has-predictableresource-urls---it-returns-http-response-codes-to-indicate-errors---it-alsoaccepts-and-returns-json-in-the-http-body---you-can-use-your-favoritehttprest-library-for-your-programming-language-to-use-rebillys-api-oryou-can-use-one-of-our-sdks-currently-available-in-phphttpsgithub-comrebillyrebillyphpand-chttpsgithub-comrebillyrebillydotnetclient--authenticationwhen-you-sign-up-for-an-account-you-are-given-your-first-api-key-you-can-generate-additional-api-keys-and-delete-api-keys-as-you-mayneed-to-rotate-your-keys-in-the-future--you-authenticate-to-therebilly-api-by-providing-your-secret-key-in-the-request-header-rebilly-offers-three-forms-of-authentication--private-key-json-web-tokens-andpublic-key--private-key-authenticates-each-request-by-searching-for-the-presenceof-an-http-header-rebapikey--jwt-authenticates-each-request-by-the-http-header-authorization--public-key-authenticates-by-the-http-header-rebauth-read-more-on-this-below-rebilly-also-offers-json-web-tokens-jwt-authentication-where-you-can-controlthe-specific-granular-permissions-and-expiration-for-that-jwt---we-call-our-resourcefor-generating-jwt-sessionstagsessions-rebilly-also-has-a-clientside-authentication-scheme-that-uses-anapiuser-and-hmacsha1-signature-only-for-the-tokens-resource-sothat-you-may-safely-create-tokens-from-the-clientside-without-compromisingyour-secret-keys-never-share-your-secret-keys--keep-them-guarded-and-secure-the-clientside-authentication-scheme-uses-one-http-header-named-rebauth--redocinject-securitydefinitions--php-sdkfor-all-php-sdk-examples-provided-in-this-spec-you-will-need-to-configure-client-you-may-do-it-like-thisphpclient--new-rebillyclient----apikey--yourapikeyhere----baseurl--httpsapi-rebilly-com
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
---