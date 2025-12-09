# Documentación API Users

Este api permite una administración básica de usuarios que se almacenan en memoria usando la tecnológia de Python y Flask

### Métodos soportados
- **GET**
- **POST**

### Ruta principal API
- **/V1/users**

### GET
- **endpoint**: /V1/users
- **Http Codes Response:**
    -200 ok
    -500 internal server error

- **JSON schema Response:**

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Generated schema for Root",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "age": {
        "type": "number"
      },
      "name": {
        "type": "string"
      }
    },
    "required": [
      "age",
      "name"
    ]
  }
}
```

- **Example Response:**

```json
{
  [
  {
    "age": 34,
    "name": "esteban"
  },
  {
    "age": 22,
    "name": "karen"
  },
  {
    "age": 20,
    "name": "Lili"
  }
]
```

### POST
> inserta un usuario en el modelo de negocio

- **endpoint**: /V1/users
- **HTTP Codes Responde:**
    - 201 Creates
    - 400
        - empty body
        - bad data type
        - incomplete body
    - 500 internal server error

- **JSON Schema Body:**
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Schema Body API",
  "type": "object",
  "items": {
    "type": "object",
    "properties": {
      "age": {
        "type": "number"
      },
      "name": {
        "type": "string"
      }
    },
    "required": [
      "age",
      "name"
    ]
  }
```

- **Example Body**
```json
{
    "age": 34,
    "name": "esteban"
}
```
