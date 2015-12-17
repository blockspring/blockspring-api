# User

1. [Get User Info](#)


## Get User Info

Get information about the current user.

### Endpoint

`GET /v0/me`

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
  "id": 3,
  "name": "Jason Tokoph",
  "username": "jtokoph",
  "organization": {
    "name": "Blockspring",
    "subdomain": "blockspring",
    "url": "https://api.blockspring.com/v0/organization?access_token={access_token}"
  },
  "url": "https://api.blockspring.com/v0/me?access_token={access_token}",
  "favorites_url": "https://api.blockspring.com/v0/favorites?access_token={access_token}"
}
```
