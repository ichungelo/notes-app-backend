# API Spec

simple note API for personal usage

## POST NOTES

Request:
- Method: POST
- Path: `/notes`
- Body:
```json
{
 "title": "string",
 "tags": ["string", "string"],
 "body": "string"
}
```

Response: 
```json
{
  "status": "string",
  "message": "string",
  "data": {
    "noteId": "string, unique"
  }
}
```

## GET ALL NOTES

Request:
- Method: GET
- Path: `/notes`

Response: 
```json
{
  "status": "string",
  "data": {
    "notes": [
      {
        "id":"string, unique",
        "title":"string",
        "createdAt":"date",
        "updatedAt":"date",
        "tags":[
          "string",
          "string"
        ],
        "body":"string"
      },
      {
        "id":"string, unique",
        "title":"string",
        "createdAt":"date",
        "updatedAt":"date",
        "tags":[
          "string",
          "string"
        ],
        "body":"string"
      }
    ]
  }
}
```

## EDIT NOTE

Request:
- Method: PUT
- Path: `/notes/{id}`
- Body:
```json
{
 "title": "string",
 "tags": ["string", "string"],
 "body": "string"
}
```

Response: 
```json
{
  "status": "string",
  "message": "string",
}
```

## DELETE NOTE

Request:
- Method: DELETE
- Path: `/notes/{id}`

Response: 
```json
{
  "status": "string",
  "message": "string"
}
```