# Server Status Backend

Express API for the server status app.

## Stack?

- Express as the backbone
- Mongoose used to interface with MongoDB

## API

|Method|Endpoint|Description|
|-|-|-|
|GET|/servers|Returns information for all servers|
|GET|/servers/:id|Returns information for a spesific server|
|POST|/servers|Adds a new server|
|PUT|/servers/:id|Updates the status of a server|
|DELETE|/servers/:id|Removes a spesific server|

### GET /servers

Returns an array of server status objects

```json
[
  {
    "id": "[INSERT ID HERE]",
    "name": "Alpha",
    "location": "Helsinki",
    "status": "running",
    "updated": "2024-02-13T09:40:39Z",
    "created": "2024-02-13T09:40:39Z"
  }, {
    "id": "[INSERT ID HERE]",
    "name": "Beta",
    "location": "Stockholm",
    "status": "starting",
    "updated": "2024-02-13T09:40:39Z",
    "created": "2024-02-13T09:40:39Z"
  }
]
```

### GET /servers/:id

Returns information for a spesific server

```json
{
  "id": "[INSERT ID HERE]",
  "name": "Alpha",
  "location": "Helsinki",
  "status": "running",
  "updated": "2024-02-13T09:40:39Z",
  "created": "2024-02-13T09:40:39Z"
}
```

### POST /servers

Adds a new server

```json
{
  "name": "Alpha",
  "location": "Helsinki"
}
```

### PUT /servers/:id

Updates the status for a server

```json
{
  "status": "down",
}
```

### DELETE /servers/:id

Deletes a server

## Server model

|Field|Type|Required|Default|Description|
|-|-|-|-|-|
|id|ObjectID||new ObjectId|ID of the object|
|name|string|yes||Name of the server|
|location|string|yes||Location of the server|
|status|string||unknown|Status of the server|
|updated|Date||Date.now|When the status was last changed|
|created|Date||Date.now|When the server was created|
