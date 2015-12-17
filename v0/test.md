# Test

1. [Test GET](#test-get)
2. [Test POST](#test-post)

## Test GET

Test your API client's GET requests

### Endpoint

`GET /v0/marco`

### Parameters

| Name | Type | Description|
| --- | --- | --- |
| N/A | N/A | N/A |

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

```javascript
{
  "shout": "POLO!"
}
```

## Test POST

Test your API client's POST requests

### Endpoint

`POST /v0/echo`

### Parameters

Post any JSON object to have it echoed back to you.

#### Example

```javascript
{
  "this": {
    "is": "too",
    "cool": ["for", "school"]
  },
  "wow": 9001
}
```

### Response

```http
Status: 200 OK
X-Blockspring-Api-Version: v0
```

```javascript
{
  "this": {
    "is": "too",
    "cool": ["for", "school"]
  },
  "wow": 9001
}
```
