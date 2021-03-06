---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets List referrers
  description: Lists referrers with the desired columns/attributes.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/items/sales_prices/{id}/referrers:
    get:
      summary: List activated referrers
      description: Lists all activated referrers for a sales price. The ID of the
        sales price must be specified.
      operationId: getRestItemsSalesPricesReferrers
      x-api-path-slug: restitemssales-pricesidreferrers-get
      parameters:
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - List
      - Activated
      - Referrers
  /rest/orders/referrers:
    get:
      summary: List referrers
      description: Lists referrers with the desired columns/attributes.
      operationId: getRestOrdersReferrers
      x-api-path-slug: restordersreferrers-get
      parameters:
      - in: query
        name: columns
        description: The desired columns/attributes of the order referrer to be loaded
      responses:
        200:
          description: OK
      tags:
      - List
      - Referrers
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