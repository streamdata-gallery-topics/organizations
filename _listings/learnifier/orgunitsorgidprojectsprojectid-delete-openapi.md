---
swagger: "2.0"
x-collection-name: Learnifier
x-complete: 0
info:
  title: Learnifier Deletes the project
  version: 1.1.0
  description: Deletes the project. The project can only be deleted if the project
    do not contain any participants.
host: learnifier.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /extorgunit:
    get:
      summary: Get Organization Unit with External Id
      description: Returns information about the organization unit with the specified
        external id.
      operationId: extorgunit.get
      x-api-path-slug: extorgunit-get
      parameters:
      - in: query
        name: extid
        description: The external id of the organization unit
      responses:
        200:
          description: OK
      tags:
      - Organizations
  /orgunits:
    get:
      summary: Organization Units
      description: |-
        The orgunits endpoint returns information about the available organization units (orgunits).
        The response includes the display name, internal and external id and client number.
      operationId: orgunits.get
      x-api-path-slug: orgunits-get
      responses:
        200:
          description: OK
      tags:
      - Organizations
    post:
      summary: Adds an Organization Unit
      description: Adds an Organization Unit
      operationId: orgunits.post
      x-api-path-slug: orgunits-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Organizations
  /orgunits/{orgid}:
    get:
      summary: Get Organization Unit
      description: |-
        Returns information about the specified organization unit.
        The response includes the display name, internal and external id and client number.
      operationId: orgunits.orgid.get
      x-api-path-slug: orgunitsorgid-get
      parameters:
      - in: path
        name: orgid
        description: Id of the organization unit
      responses:
        200:
          description: OK
      tags:
      - Organizations
    patch:
      summary: Updates an Organization Unit
      description: Adds an Organization Unit
      operationId: orgunits.orgid.patch
      x-api-path-slug: orgunitsorgid-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orgid
      responses:
        200:
          description: OK
      tags:
      - Organizations
  /orgunits/{orgid}/projects:
    get:
      summary: Organization Unit Projects
      description: Returns the available projects for the organization unit
      operationId: orgunits.orgid.projects.get
      x-api-path-slug: orgunitsorgidprojects-get
      parameters:
      - in: path
        name: orgid
        description: Id of the organization unit
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Projects
    post:
      summary: Create project
      description: Creates a new project
      operationId: orgunits.orgid.projects.post
      x-api-path-slug: orgunitsorgidprojects-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: orgid
        description: Id of the organization unit
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Projects
  /orgunits/{orgid}/projects/{projectid}:
    delete:
      summary: Deletes the project
      description: Deletes the project. The project can only be deleted if the project
        do not contain any participants.
      operationId: orgunits.orgid.projects.projectid.delete
      x-api-path-slug: orgunitsorgidprojectsprojectid-delete
      parameters:
      - in: path
        name: orgid
        description: Id of the organization unit
      - in: path
        name: projectid
        description: Id of the project
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Projects
      - Projectid
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