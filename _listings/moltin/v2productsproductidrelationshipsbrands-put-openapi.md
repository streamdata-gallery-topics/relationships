---
swagger: "2.0"
x-collection-name: moltin
x-complete: 0
info:
  title: Moltin API Update Product <=> Brands Relationships
  description: Here you can set relations `Brand`'s to a product. The result of this
    request will set relationships between product and the specified brnads in teh
    payload and remove any other relations the product had with brands.
  version: 1.0.0
host: api.moltin.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/products/{productID}/relationships/variations:
    put:
      summary: Update Product <=> Variations Relationships
      description: '`Product Variation`''s specified in the payload willbe related
        to the `Product` any relatiosnhips to `Product Variation`''s **NOT** specified
        in payload will be removed.'
      operationId: V2ProductsRelationshipsVariationsByProductIDPut
      x-api-path-slug: v2productsproductidrelationshipsvariations-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Products
      - Variations
      - Relationships
    post:
      summary: Create Product <=> Variations Relationships
      description: Here you can add and remove `Product Variation`'s to a product.
        `Product Variation`'s specified in the payload willbe related to the product.
      operationId: V2ProductsRelationshipsVariationsByProductIDPost
      x-api-path-slug: v2productsproductidrelationshipsvariations-post
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Products
      - Variations
      - Relationships
    delete:
      summary: Delete Product <=> Variations Relationships
      description: Here you can add and remove `Product Variation`'s to a product.
        Only relationships to `Product Variation`'s specified in the payload will
        be removed.
      operationId: V2ProductsRelationshipsVariationsByProductIDDelete
      x-api-path-slug: v2productsproductidrelationshipsvariations-delete
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Products
      - Variations
      - Relationships
  /v2/products/{productID}/relationships/files:
    put:
      summary: Update Products <=> Files Relationships
      description: '`File`''s specified in the payload willbe related to the product
        any relatiosnhips to `File`''s **NOT** specified in payload will be removed.'
      operationId: V2ProductsRelationshipsFilesByProductIDPut
      x-api-path-slug: v2productsproductidrelationshipsfiles-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Productss
      - Files
      - Relationships
    post:
      summary: Create Products <=> Files Relationships
      description: Here you can add `File`'s to a product. `File`'s specified in the
        payload willbe related to the product.
      operationId: V2ProductsRelationshipsFilesByProductIDPost
      x-api-path-slug: v2productsproductidrelationshipsfiles-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Productss
      - Files
      - Relationships
  /v2/collections/{collectionID}/relationships/collections:
    post:
      summary: Create Collection Relationships
      description: Create collection relationships.
      operationId: V2CollectionsRelationshipsCollectionsByCollectionIDPost
      x-api-path-slug: v2collectionscollectionidrelationshipscollections-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: collectionID
      - in: header
        name: Content-Type
      responses:
        200:
          description: Successful response
      tags:
      - Collection
      - Relationships
  /v2/categories/{categoryID}/relationships/children:
    put:
      summary: Update Child Category Relationships
      description: Update child category relationships.
      operationId: V2CategoriesRelationshipsChildrenByCategoryIDPut
      x-api-path-slug: v2categoriescategoryidrelationshipschildren-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: categoryID
      - in: header
        name: Content-Type
      responses:
        200:
          description: Successful response
      tags:
      - Child
      - Category
      - Relationships
    delete:
      summary: Delete Child Category Relationships
      description: Delete child category relationships.
      operationId: V2CategoriesRelationshipsChildrenByCategoryIDDelete
      x-api-path-slug: v2categoriescategoryidrelationshipschildren-delete
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: categoryID
      - in: header
        name: Content-Type
      responses:
        200:
          description: Successful response
      tags:
      - Child
      - Category
      - Relationships
  /categories/{categoryID}/relationships/children:
    post:
      summary: Create Child Category Relationships
      description: Create child category relationships.
      operationId: CategoriesRelationshipsChildrenByCategoryIDPost
      x-api-path-slug: categoriescategoryidrelationshipschildren-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: categoryID
      - in: header
        name: Content-Type
      responses:
        200:
          description: Successful response
      tags:
      - Child
      - Category
      - Relationships
  /v2/products/{productID}/relationships/brands:
    put:
      summary: Update Product <=> Brands Relationships
      description: Here you can set relations `Brand`'s to a product. The result of
        this request will set relationships between product and the specified brnads
        in teh payload and remove any other relations the product had with brands.
      operationId: V2ProductsRelationshipsBrandsByProductIDPut
      x-api-path-slug: v2productsproductidrelationshipsbrands-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: productID
      responses:
        200:
          description: Successful response
      tags:
      - Products
      - Brandss
      - Relationships
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