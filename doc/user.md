# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
  "username": "dikiomen",
  "password": "rahasia",
  "name": "Ilham Basudara"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "dikiomen",
    "name": "Ilham Basudara"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username must not blank, ..."
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
  "username": "dikiomen",
  "password": "rahasia"
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "dikiomen",
    "name": "Ilham Basudara",
    "token": "uuid"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Username or password, ..."
}
```

## Get User

Endpoint : GET /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
  "data": {
    "username": "dikiomen",
    "name": "Ilham Basudara"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Update User

Endpoint : PATCH /api/users/current

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
  "password": "rahasia", // tidak wajib
  "name": "Ilham Basudara" // tidak wajib
}
```

Response Body (Success) :

```json
{
  "data": {
    "username": "dikiomen",
    "name": "Ilham Basudara"
  }
}
```

Response Body (Failed) :

```json
{
  "errors": "Unauthorized, ..."
}
```

## Logout User

Endpoint : DELETE /api/users/current

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
  "errors": "Unauthorized, ..."
}
```
