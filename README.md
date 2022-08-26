# API Spec

## Create Product

Request: 
- Method: POST
- Endpoint: `/api/products`
- Header: 
    - Content-Type: application/json
    - Accept: application/json
- Body:
```json
{
  "id": "String, unique",
  "name": "String, not empty",
  "price": "Long, not 0",
  "quantity": "Int, not 0"
}
```
Response:
```json
{
  "code": "Int, HTTP response code",
  "status": "String, not empty",
  "data": {
    "id": "String, unique",
    "name": "String, not empty",
    "price": "Long, not 0",
    "quantity": "Int, not 0",
    "created_at": "Date, set once",
    "updated_at": "Date, nullable"
  }
}
```

## Get Product
Request:
- Method: GET
- Endpoint: `/api/products/{id}`
- Header:
  - Accept: application/json

Response:
```json
{
  "code": "Int, HTTP response code",
  "status": "String, not empty",
  "data": {
    "id": "String, unique",
    "name": "String, not empty",
    "price": "Long, not 0",
    "quantity": "Int, not 0",
    "created_at": "Date, set once",
    "updated_at": "Date, nullable"
  }
}
```
## Get All Products
Request:
- Method: GET
- Endpoint: `/api/products`
- Header:
  - Accept: application/json
- Query Param:
  - size: Int
  - page: Int

Response:
```json
{
  "code": "Int, HTTP response code",
  "status": "String, not empty",
  "data": [
    {
      "id": "String, unique",
      "name": "String, not empty",
      "price": "Long, not 0",
      "quantity": "Int, not 0",
      "created_at": "Date, set once",
      "updated_at": "Date, nullable"
    }
  ]
}
```

## Update Product
Request:
- Method: PUT
- Endpoint: `/api/products/{id}`
- Header:
  - Content-Type: application/json
  - Accept: application/json
- Body:
```json
{
  "name": "String, not empty",
  "price": "Long, not 0",
  "quantity": "Int, not 0"
}
```
Response:
```json
{
  "code": "Int, HTTP response code",
  "status": "String, not empty",
  "data": {
    "id": "String, unique",
    "name": "String, not empty",
    "price": "Long, not 0",
    "quantity": "Int, not 0",
    "created_at": "Date, set once",
    "updated_at": "Date, nullable"
  }
}
```


## Delete Product
Request:
- Method: DELETE
- Endpoint: `/api/products/{id}`
- Header:
  - Accept: application/json

Response:
```json
{
  "code": "Int, HTTP response code",
  "status": "String, not empty",
  "data": "String"
}
```