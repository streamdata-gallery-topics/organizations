---
swagger: "2.0"
x-collection-name: Disqus
x-complete: 0
info:
  title: Disqus Organizations ListAdmins
  description: Organizations ListAdmins
  termsOfService: https://docs.disqus.com/kb/terms-and-policies/
  version: 1.0.0
host: disqus.com
basePath: api/3.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/listAdmins.json:
    get:
      summary: Organizations ListAdmins
      description: Organizations ListAdmins
      operationId: organizations-listadmins
      x-api-path-slug: organizationslistadmins-json-get
      parameters:
      - in: query
        name: organization
        description: Looks up an organization by ID You must be an admin on the selected
          organization
        type: string
      responses:
        200:
          description: OK
      tags:
      - Comments
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