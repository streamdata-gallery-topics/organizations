---
swagger: "2.0"
x-collection-name: CloudFlare
x-complete: 0
info:
  title: CloudFlare Update an existing Organization
  version: 1.0.0
  description: Update an existing Organization
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/:identifier:
    get:
      summary: Get information about a specific organization that you are a member
        of
      description: Get information about a specific organization that you are a member
        of
      operationId: cloudflare-organizations-api
      x-api-path-slug: organizationsidentifier-get
      responses:
        200:
          description: OK
      tags:
      - Organizations
    patch:
      summary: Update an existing Organization
      description: Update an existing Organization
      operationId: cloudflare-organizations-api
      x-api-path-slug: organizationsidentifier-patch
      parameters:
      - in: query
        name: name
        description: Organization NamettttttttttttttCloudFlare, Inc
      - in: header
        name: X-AUTH-EMAIL
        description: Email address associated with your account
      - in: header
        name: X-AUTH-KEY
        description: API key generated on the My Account page
      responses:
        200:
          description: OK
      tags:
      - Organizations
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