# Address API Spec

## Create Address

Endpoint : POST /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "12312"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "postal_code is required"
}
```

## Get Address

Endpoint : GET /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Address is not found"
}
```

## Update Address

Endpoint : PUT /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "street": "Jalan apa",
  "city": "Kota apa",
  "province": "Provinsi apa",
  "country": "Negara apa",
  "postal_code": "12312"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id": 1,
    "street": "Jalan apa",
    "city": "Kota apa",
    "province": "Provinsi apa",
    "country": "Negara apa",
    "postal_code": "12312"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "postal_code is required"
}
```

## Remove Address

Endpoint : DELETE /api/contacts/:idContact/addresses/:idAddress

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": "Ok"
}
```

Response Body (Failed) :

```json
{
  "errors": "Address is not found"
}
```

## List Address

Endpoint : GET /api/contacts/:idContact/addresses

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": [
    {
      "id": 1,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "12312"
    },
    {
      "id": 2,
      "street": "Jalan apa",
      "city": "Kota apa",
      "province": "Provinsi apa",
      "country": "Negara apa",
      "postal_code": "12312"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors": "Contact is not found"
}
```
