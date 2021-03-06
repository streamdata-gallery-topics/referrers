---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez updates the content of a sack
  version: 1.0.0
  description: Updates the content of a sack.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/Peppermint:
    post:
      summary: Submits a referral to dezrez legal
      description: Submits a referral to dezrez legal.
      operationId: Peppermint_SubmitReferralByreferralDataContract
      x-api-path-slug: apipeppermint-post
      parameters:
      - in: body
        name: referralDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Submits
      - Referral
      - To
      - Dezrez
      - Legal
  /api/role/createreferralevent:
    post:
      summary: Creates a referral event on the role
      description: Creates a referral event on the role.
      operationId: Role_CreateReferralEventByreferralData
      x-api-path-slug: apirolecreatereferralevent-post
      parameters:
      - in: body
        name: referralData
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Referral
      - Event
      - "On"
      - Role
  /api/coreplatformstate/{stateItemReference}:
    delete:
      summary: Clears a state item.
      description: Clears a state item..
      operationId: CorePlatformState_ClearStateItemBystateItemReference
      x-api-path-slug: apicoreplatformstatestateitemreference-delete
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: stateItemReference
        description: The state item reference
      responses:
        200:
          description: OK
      tags:
      - Clears
      - State
      - Item
  /api/documentgeneration/deletesackcontent/{sackReference}/{envelopereference}:
    get:
      summary: "deletes an envelope from the the content of a sack \r\nDeprecated
        in favour of the DELETE verb"
      description: "Deletes an envelope from the the content of a sack \r\ndeprecated
        in favour of the delete verb."
      operationId: DocumentGeneration_DeleteSackContentDeprecatedBysackReferenceByenvelopereference
      x-api-path-slug: apidocumentgenerationdeletesackcontentsackreferenceenvelopereference-get
      parameters:
      - in: path
        name: envelopereference
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Deletes
      - Envelope
      - From
      - The
      - Content
      - Of
      - Sack
      - Deprecated
      - In
      - Favour
      - Of
      - DELETE
      - Verb
  /api/documentgeneration/envelopecontent/{sackReference}/{envelopereference}/{documentreference}:
    delete:
      summary: deletes an document from an envelope
      description: Deletes an document from an envelope.
      operationId: DocumentGeneration_DeleteEnvelopeContentBysackReferenceByenvelopereferenceBydocumentreference
      x-api-path-slug: apidocumentgenerationenvelopecontentsackreferenceenvelopereferencedocumentreference-delete
      parameters:
      - in: path
        name: documentreference
      - in: path
        name: envelopereference
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Deletes
      - Document
      - From
      - Envelope
  /api/documentgeneration/printsackcontent/{sackReference}/{envelopereference}:
    get:
      summary: Prints an envelope from a sack
      description: Prints an envelope from a sack.
      operationId: DocumentGeneration_PrintSackContentBysackReferenceByenvelopereference
      x-api-path-slug: apidocumentgenerationprintsackcontentsackreferenceenvelopereference-get
      parameters:
      - in: path
        name: envelopereference
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Prints
      - Envelope
      - From
      - Sack
  /api/documentgeneration/processsackcontent/{sackReference}:
    get:
      summary: processes the content of the sack
      description: Processes the content of the sack.
      operationId: DocumentGeneration_ProcessSackContentBysackReference
      x-api-path-slug: apidocumentgenerationprocesssackcontentsackreference-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Processes
      - Content
      - Of
      - Sack
  /api/documentgeneration/sack/{sackReference}:
    delete:
      summary: deletes an envelope from the the content of a sack
      description: Deletes an envelope from the the content of a sack.
      operationId: DocumentGeneration_DeleteSackBysackReference
      x-api-path-slug: apidocumentgenerationsacksackreference-delete
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Deletes
      - Envelope
      - From
      - The
      - Content
      - Of
      - Sack
  /api/documentgeneration/sackcontent/{sackReference}:
    get:
      summary: Returns the detail of the all outstanding sacks
      description: Returns the detail of the all outstanding sacks.
      operationId: DocumentGeneration_GetSackContentBysackReference
      x-api-path-slug: apidocumentgenerationsackcontentsackreference-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Detail
      - Of
      - ""
      - Outstanding
      - Sacks
  /api/documentgeneration/sackcontent/{sackReference}/{envelopereference}:
    delete:
      summary: deletes an envelope from the the content of a sack
      description: Deletes an envelope from the the content of a sack.
      operationId: DocumentGeneration_DeleteSackContentBysackReferenceByenvelopereference
      x-api-path-slug: apidocumentgenerationsackcontentsackreferenceenvelopereference-delete
      parameters:
      - in: path
        name: envelopereference
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Deletes
      - Envelope
      - From
      - The
      - Content
      - Of
      - Sack
  /api/documentgeneration/updateemailsackcontent/{sackReference}:
    post:
      summary: updates the content of a sack
      description: Updates the content of a sack.
      operationId: DocumentGeneration_UpdateEmailSackContentBysackReferenceByemail
      x-api-path-slug: apidocumentgenerationupdateemailsackcontentsackreference-post
      parameters:
      - in: body
        name: email
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: sackReference
      responses:
        200:
          description: OK
      tags:
      - Updates
      - Content
      - Of
      - Sack
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