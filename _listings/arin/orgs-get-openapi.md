---
swagger: "2.0"
x-collection-name: ARIN
x-complete: 0
info:
  title: Organization API Manages organizations
  description: ""
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
host: www.arin.net
basePath: /regrws/core/v1
paths:
  /orgs:
    get:
      summary: Manages organizations
      description: ""
      operationId: organizations
      x-api-path-slug: orgs-get
      parameters:
      - in: query
        name: dba
        description: the name the organization does business as
        type: string
        format: string
      - in: query
        name: handle
        description: the handle of the organization
        type: string
        format: string
      - in: query
        name: name
        description: the name of organization
        type: string
        format: string
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