---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Check specified key codes exist in branch
  version: 1.0.0
  description: Check specified key codes exist in branch.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/agency/portalconfigurations:
    get:
      summary: Get a list of portal configurations for the brand within a branch.
      description: Get a list of portal configurations for the brand within a branch..
      operationId: Agency_PortalConfigurationsBypageSizeBypageNumber
      x-api-path-slug: apiagencyportalconfigurations-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Portal
      - Configurationsthe
      - Brand
      - Within
      - Branch
  /api/agency/updateportalcustomisation:
    put:
      summary: "THIS IS A TEMPORARY ENDPOINT TO Update a portal customisation against
        a brand within a branch.\r\nPLEASE NOTE: This will be replaced by a FE Tool
        in future. If not, Security must be improved."
      description: "This is a temporary endpoint to update a portal customisation
        against a brand within a branch.\r\nplease note: this will be replaced by
        a fe tool in future. if not, security must be improved.."
      operationId: Agency_UpdatePortalCustomisationByportalCustomisation
      x-api-path-slug: apiagencyupdateportalcustomisation-put
      parameters:
      - in: body
        name: portalCustomisation
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - THIS
      - IS
      - TEMPORARY
      - ENDPOINT
      - TO
      - ""
      - Portal
      - Customisation
      - Against
      - Brand
      - Within
      - Branch
      - PLEASE
      - 'NOTE:'
      - This
      - Will
      - Be
      - Replaced
      - By
      - FE
      - Tool
      - In
      - Future
      - ""
      - If
      - Not
      - ""
      - Security
      - Must
      - Be
      - Improved
  /api/branch/{id}:
    get:
      summary: Get a Branch by its id.
      description: Get a branch by its id..
      operationId: Branch_GetByid
      x-api-path-slug: apibranchid-get
      parameters:
      - in: path
        name: id
        description: The id of the Branch to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Branch
      - By
      - Its
      - Id
  /api/branch/{id}/Brandings:
    get:
      summary: Get a Branch brandings by its id.
      description: Get a branch brandings by its id..
      operationId: Branch_BrandingsByid
      x-api-path-slug: apibranchidbrandings-get
      parameters:
      - in: path
        name: id
        description: The id of the Branch brandings  to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Branch
      - Brandings
      - By
      - Its
      - Id
  /api/branch/{id}/administrators:
    get:
      summary: Get Branch administrators by its id.
      description: Get branch administrators by its id..
      operationId: Branch_AdministratorsByid
      x-api-path-slug: apibranchidadministrators-get
      parameters:
      - in: path
        name: id
        description: The id of the Branch administrators to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Branch
      - Administrators
      - By
      - Its
      - Id
  /api/branch/{id}/members:
    get:
      summary: Get Branch members by its id.
      description: Get branch members by its id..
      operationId: Branch_MembersByid
      x-api-path-slug: apibranchidmembers-get
      parameters:
      - in: path
        name: id
        description: The id of the Branch members to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Branch
      - Members
      - By
      - Its
      - Id
  /api/branch/{id}/addnegotiator:
    post:
      summary: Adds a negoatiator to a branch
      description: Adds a negoatiator to a branch.
      operationId: Branch_AddNegotiatorByidBycommand
      x-api-path-slug: apibranchidaddnegotiator-post
      parameters:
      - in: body
        name: command
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Negoatiator
      - To
      - Branch
  /api/branch/{id}/getbrand:
    get:
      summary: Get a specific brand by brandId or default brand within a branch if
        brandId is not supplied.
      description: Get a specific brand by brandid or default brand within a branch
        if brandid is not supplied..
      operationId: Branch_GetBranchBrandByidBybrandId
      x-api-path-slug: apibranchidgetbrand-get
      parameters:
      - in: query
        name: brandId
        description: The id of brand to get
      - in: path
        name: id
        description: The id of a branch
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Specific
      - Brand
      - By
      - BrandId
      - Default
      - Brand
      - Within
      - Branch
      - If
      - BrandId
      - Is
      - Not
      - Supplied
  /api/branch/updatefee:
    put:
      summary: Add or update fee for logged in branch.
      description: Add or update fee for logged in branch..
      operationId: Branch_UpdateBranchFeeByfeeDataContract
      x-api-path-slug: apibranchupdatefee-put
      parameters:
      - in: body
        name: feeDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Update
      - Feelogged
      - In
      - Branch
  /api/branch/deletefee/{defaultFeeId}:
    delete:
      summary: Delete fee for logged in branch.
      description: Delete fee for logged in branch..
      operationId: Branch_DeleteBranchFeeBydefaultFeeId
      x-api-path-slug: apibranchdeletefeedefaultfeeid-delete
      parameters:
      - in: path
        name: defaultFeeId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Feelogged
      - In
      - Branch
  /api/branch/fees:
    get:
      summary: Get fees for logged in branch.
      description: Get fees for logged in branch..
      operationId: Branch_GetFeesBytransactionTypeBydefaultOnly
      x-api-path-slug: apibranchfees-get
      parameters:
      - in: query
        name: defaultOnly
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: transactionType
      responses:
        200:
          description: OK
      tags:
      - Feeslogged
      - In
      - Branch
  /api/branch/scheduledmailmerges:
    get:
      summary: Get all scheduled mail merges for the logged in branch.
      description: Get all scheduled mail merges for the logged in branch..
      operationId: Branch_GetScheduledMailMergesBypageSizeBypageNumber
      x-api-path-slug: apibranchscheduledmailmerges-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Scheduled
      - Mail
      - Mergesthe
      - Logged
      - In
      - Branch
  /api/branch/checkkeycodesexist:
    get:
      summary: Check specified key codes exist in branch
      description: Check specified key codes exist in branch.
      operationId: Branch_CheckKeycodesExistBykeyCodes
      x-api-path-slug: apibranchcheckkeycodesexist-get
      parameters:
      - in: query
        name: keyCodes
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Check
      - Specified
      - Key
      - Codes
      - Exist
      - In
      - Branch
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